<script>
    import Router from 'svelte-spa-router';

    import Navbar from './components/navbar.svelte';

    import Index from './routes/Index.svelte';
    import NotFound from './routes/NotFound.svelte';

    let routes = {
        "/": Index,
        
        "*": NotFound,
    }
</script>

<Navbar/>

<main>
    <Router {routes}/>
</main>
