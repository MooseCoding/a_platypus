<script lang="ts">
	import '../app.css';
	let { children } = $props();

	import NavBar from '$lib/NavBar.svelte';
	import Footer from '$lib/Footer.svelte'; 
</script>

<NavBar /> 

{@render children()}

<Footer /> 