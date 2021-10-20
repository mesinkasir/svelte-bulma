<script>
	import Beranda from "./Beranda.svelte";
	import Profile from "./Profile.svelte";
	import Toko from "./Toko.svelte";
	import Resto from "./Resto.svelte";
	import Pricing from "./Pricing.svelte";
	import Contact from "./Contact.svelte";
	export let menu = 1;
</script>
<nav id="menu" class="navbar" role="navigation" aria-label="main navigation">
	<div class="navbar-brand">
	  <a class="navbar-item" href="/" on:click|preventDefault={() => (menu = 1)}>
		<img alt="toko online shop whatsapp" 
		src="https://whatshop.vercel.app/static/76ab27c35420dc20ecbd3d70623dda31/af9bc/logos.avif" 
		/>
	  </a>
	  <button role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
		<span aria-hidden="true"></span>
		<span aria-hidden="true"></span>
		<span aria-hidden="true"></span>
	  </button>
	</div>
	<div id="navbarBasicExample" class="navbar-menu">
	  <div class="navbar-start">
			<a class="navbar-item" href="/" on:click|preventDefault={() => (menu = 1)}>Home</a>
		
			<a class="navbar-item" href="/" on:click|preventDefault={() => (menu = 2)}>Fitur</a>
			<a class="navbar-item" href="/" on:click|preventDefault={() => (menu = 3)}>Toko</a>
			<a class="navbar-item" href="/" on:click|preventDefault={() => (menu = 4)}>Resto</a>
			<a class="navbar-item" href="/" on:click|preventDefault={() => (menu = 5)}>Pricing</a>
			<a class="navbar-item" href="/" on:click|preventDefault={() => (menu = 6)}>Contact</a>
	  </div>
	  <div class="navbar-end">
		<div class="navbar-item">
		  <div class="buttons">
			<a href="https://play.google.com/store/apps/details?id=com.axcora.whatshop" class="button is-primary">
			  <strong>PlayStore</strong>
			</a>
			<a href="https://github.com/mesinkasir/svelte-bulma" class="button is-dark">
			  Github
			</a>
		  </div>
		</div>
	  </div>
	</div>
  </nav>

{#if menu === 1}
<Beranda />
{:else if menu === 2}
<Profile />
{:else if menu === 3}
<Toko />
{:else if menu === 4}
<Resto />
{:else if menu === 5}
<Pricing />
{:else if menu === 6}
<Contact />
{:else}
<h1>
	404 Page Not Found
</h1>
{/if}

