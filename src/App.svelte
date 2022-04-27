<script>
 // routing imports
 import {
	 Route,
	 router
 } from 'tinro';

 // page imports
 import Home from './Home/Home.svelte';
 import Downloads from './Downloads/Downloads.svelte';
 import About from './About/About.svelte';


 // component imports
 import Edition from './Home/Edition.svelte';
 import Footer from './Footer.svelte';

 // Go to page top when navigating to a new page
 router.subscribe(_ => window.scrollTo(0,0));

// Define edition objects here
 const lxqt = {
     "icon": "/images/lxqt-logo.png",
     "photo": "/images/lxqt.png",
     "name": "Cereus LxQt",
     "int_link": "/lxqt",
     "description": "LxQt is a lightweight environment that runs on low-resources",
     "dl_link": "https://sourceforge.net/projects/cereus-linux/",
     "arch": "i686 y amd64",
     "is_testing": true
 };

 const xfce = {
     "icon": "/images/xfce-logo.png",
     "photo": "/images/xfce.png",
     "name": "Cereus Xfce",
     "int_link": "/xfce",
     "description": "Xfce is a lightweight environment that runs on low-resources PCs, different to LxQt, Xfce is more personalizable",
     "dl_link": "",
     "arch": "i686 y amd64",
     "is_testing": false
 };

 const plasma = {
     "icon": "/images/plasma-logo.png",
     "photo": "/images/plasma.png",
     "name": "Cereus Plasma",
     "int_link": "/plasma",
     "description": "plasma is a modern and highly personalizable environment",
     "dl_link": "",
     "arch": "amd64",
     "is_testing": false
 };

 const cinnamon = {
     "icon": "/images/cinnamon-logo.png",
     "photo": "/images/cinnamon.png",
     "name": "Cereus Cinnamon",
     "int_link": "/cinnamon",
     "description": "Cinnamon is a modern and Familiar environment",
     "dl_link": "",
     "arch": "amd64",
     "is_testing": false
 }
 
</script>

<style>
 ul { list-style:none; }

 .cereus-nav { background: #4DB6AC; }

 .cereus-link:hover { background-color: #00766b; }

 .nav li ul {
     display:none; position:absolute; min-width:120px;
 }

 .nav li:hover > ul {
     background-color: #4DB6AC;
     display:block;
 }
</style>


<nav class="border-bottom cereus-nav">
    <div class="container d-flex flex-wrap justify-content-end">
      <ul class="nav">
        <li class="nav-item"><a href="/" class="nav-link cereus-link link-light px-2">Home</a></li>
        <li class="nav-item">
            <a href="/downloads" class="nav-link cereus-link link-light px-2">Downloads</a>
            <ul>
                <li><a class="text-light text-decoration-none" href="/lxqt">Lxqt</a></li>
                <li><a class="text-light text-decoration-none" href="/xfce">Xfce</a></li>
                <li><a class="text-light text-decoration-none" href="/plasma">Plasma</a></li>
                <li><a class="text-light text-decoration-none" href="/cinnamon">Cinnamon</a></li>
            </ul>
        </li>
        <li class="nav-item"><a href="/about" class="nav-link cereus-link link-light px-2">About</a></li>
        <li class="nav-item"><a href="https://sourceforge.net/p/cereus-linux/blog/" target="_blank" rel="noopener noreferrer" class="nav-link cereus-link link-light px-2">Blog</a></li>
      </ul>
    </div>
</nav>

<Route path="/">
    <Home/>
</Route>

<Route path="/downloads">
    <Downloads/>
</Route>

<Route path="/lxqt">
    <Edition {...lxqt}/>
</Route>

<Route path="/xfce">
    <Edition {...xfce}/>
</Route>

<Route path="/plasma">
    <Edition {...plasma}/>
</Route>

<Route path="/cinnamon">
    <Edition {...cinnamon}/>
</Route>

<Route path="/about">
    <About/>
</Route>

<Route fallback>Error 404 - not found jsjsjs</Route>

<!-- Footer Component -->
<Footer/>
