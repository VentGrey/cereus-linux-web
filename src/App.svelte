<script>
 // routing imports
 import {
	 Route,
	 router
 } from 'tinro';

 // page imports
 import Home from './Home/Home.svelte';
 import About from './About/About.svelte';

 // component imports
 import Footer from './Footer.svelte';

 // Go to page top when navigating to a new page
 router.subscribe(_ => window.scrollTo(0,0));
</script>

<style>
 .cereus-nav {
     background: #4DB6AC;
 }

 .cereus-link:hover {
     background-color: #00766b;
 }
</style>


<nav class="border-bottom cereus-nav">
    <div class="container d-flex flex-wrap justify-content-end">
      <ul class="nav">
        <li class="nav-item"><a href="/" class="nav-link cereus-link link-light px-2">Home</a></li>
        <li class="nav-item"><a href="#" class="nav-link cereus-link link-light px-2">Downloads</a></li>
        <li class="nav-item"><a href="/about" class="nav-link cereus-link link-light px-2">About</a></li>
        <li class="nav-item"><a href="https://sourceforge.net/p/cereus-linux/blog/" target="_blank" rel="noopener noreferrer" class="nav-link cereus-link link-light px-2">Blog</a></li>
      </ul>
    </div>
</nav>

<Route path="/">
    <Home/>
</Route>

<Route path="/about">
    <About/>
</Route>

<Route fallback>Error 404 - not found jsjsjs</Route>

<!-- Footer Component -->
<Footer/>
