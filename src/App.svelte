<script>
    import "../node_modules/materialize-css/dist/css/materialize.css";

    import { Router, Route } from "svelte-routing";
    import { setupI18n, isLocaleLoaded, locale, dir } from './services/i18n';
    import Header from './components/Layout/Header.svelte';
    import Footer from './components/Layout/Footer.svelte';
    import About from './components/Pages/About.svelte';
    import Contact from './components/Pages/Contact.svelte';
    import FrameworkGrid from './components/Frameworks/FrameworkGrid.svelte';
    import LocaleSwitcher from './components/Controllers/LocaleSwitcher.svelte';

    $: if (!$isLocaleLoaded) {
        setupI18n({ withLocale: 'en' });
    }

    $: { document.dir = $dir; }
</script>

<style>
    main { padding: 0 1rem; }
</style>

{#if $isLocaleLoaded}
<Router>
    <Header />
    <div class="container">
    <Route path="/contact" component={Contact} />
    <Route path="/about" component={About} />
    </div>
</Router>
    <LocaleSwitcher
        value={$locale}
        on:locale-changed={e => setupI18n({ withLocale: e.detail }) }
    />

    <main role="main">
        <FrameworkGrid />
    </main>

    <Footer />
{:else}
    <p>Loading...</p>
{/if}
