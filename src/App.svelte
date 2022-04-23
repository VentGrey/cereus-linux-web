<script>
 import {
	 Route,
	 router
 } from 'tinro';

 router.subscribe(_ => window.scrollTo(0,0));
</script>

<style>
 .cereus-nav {
     background: #4DB6AC;
 }
</style>


<nav class="border-bottom cereus-nav">
    <div class="container d-flex flex-wrap justify-content-end">
      <ul class="nav">
        <li class="nav-item"><a href="#" class="nav-link link-light px-2">Home</a></li>
        <li class="nav-item"><a href="#" class="nav-link link-light px-2">Downloads</a></li>
        <li class="nav-item"><a href="#" class="nav-link link-light px-2">About</a></li>
        <li class="nav-item"><a href="#" class="nav-link link-light px-2">Blog</a></li>
      </ul>
    </div>
  </nav>
