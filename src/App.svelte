<script>
    import Router from 'svelte-spa-router';

    import Navbar from './components/navbar.svelte';
    import Footer from './components/footer.svelte';

    import Home from './routes/Home.svelte';
    import NotFound from './routes/NotFound.svelte';
    import Munpia from './routes/platforms/Munpia.svelte';
    import Novelpia from './routes/platforms/Novelpia.svelte';
    import Kakaopage from './routes/platforms/Kakaopage.svelte';
    import Kakaostage from './routes/platforms/Kakaostage.svelte';
    import Navernovel from './routes/platforms/Navernovel.svelte';

    let routes = {
        "/": Home,
        "/platforms/munpia": Munpia,
        "/platforms/novelpia": Novelpia,
        "/platforms/kakaopage": Kakaopage,
        "/platforms/kakaostage": Kakaostage,
        "/platforms/navernovel": Navernovel,
        
        "*": NotFound,
    }
</script>

<div class="m-0 h-min w-screen xs:w-screen bg-gray-900">
    <div class="container mx-auto lg:w-10/12 xl:w-8/12">
        <Navbar/>

        <main>
            <Router {routes}/>
        </main>

        <Footer/>
    </div>
</div>
