<script lang="ts">
	import { onMount } from 'svelte';
    import { browser } from '$app/env';
	import Slideshow from './slideshow.svelte';

</script>

<svelte:head>
	<title>Opinion</title>
</svelte:head>

<div class="  pt-20 md:pt-20 h-full w-full bg-cover 	">
<h1  class=" bg-gray-700">Welcome to SvelteKit project Opinion</h1>
    </div>
    <br/>
<Slideshow />
    <br/>

<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
