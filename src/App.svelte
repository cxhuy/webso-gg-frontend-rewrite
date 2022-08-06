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

<div class="m-0 h-min w-min xs:w-screen bg-gray-900">
    <div class="container mx-auto lg:w-10/12 xl:w-8/12">
        <Navbar/>

        <main>
            <Router {routes}/>
        </main>
    </div>
</div>
