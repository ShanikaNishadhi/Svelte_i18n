<script>
    import { _, locale, formatDate, date, time, number} from '../../services/i18n';
   //import {time, date, number} from 'svelte-i18n'

    export let framework;

    const {
        imageUrl: src,
        awardWinCount,
        awardNominationCount: nominationCount,
        releaseDate: released,
    } = framework;

    $: title = framework[`title_${$locale}`];
</script>

<style>
    .box {
        background-color: #f7f7f7;
    }
    @media screen and (min-width:769px) {
        .box {
            height: 23rem;
        }
    }

    img {
        display: block;
        border-radius: 0.25rem;
        max-height: 100%;
        max-width: 100%;
        object-fit: cover;
    }

    .movie-title {
        margin-top: 0;
    }

    .release-date {
        padding-bottom: 0.5rem;
        margin-bottom: 0.5rem;
        border-bottom: 1px solid #e9e9e9;
    }

    .awards, .nominations {
        font-size: 0.85rem;
    }
</style>

<div class="box">
    <div class="columns is-mobile">
        <div class="column is-one-quarter img-container">
            <img {src} alt="Poster for {title}">
        </div>

        <div class="column">
            <h3 class="is-size-5 is-uppercase movie-title">{title}</h3>

            <p class="release-date">
                {$_('framework.released_at', { date: formatDate(released, { year: 'numeric' }) })}
                {$_.date(2020, 4, 10, 5 )}
            Hi how are you
            </p>
            <div>{$date(new Date(2019, 3, 24, 23, 45))}</div>

            <p class="awards">
                {$_('framework.languages', { n: awardWinCount })}
            </p>

            <p class="nominations">
                {$_('framework.rtl', { n: nominationCount })}
            </p>
        </div>
    </div>
</div>