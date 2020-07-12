<script>
    import Framework from './Framework.svelte';

    function fetchFrameworks() {
        return fetch('/data/frameworks.json')
                .then(response => response.json());
    }
</script>

{#await fetchFrameworks()}
    <p>Loading your Svelte application...</p>
{:then frameworks}
    <div class="columns is-mobile is-multiline">
        {#each frameworks as framework}
            <div class="column is-one-third-desktop is-half-tablet is-full-mobile">
                <Framework {framework} />
            </div>
        {/each}
    </div>
{:catch error}
    <p>There was a problem loading information on frameworks.</p>
{/await}