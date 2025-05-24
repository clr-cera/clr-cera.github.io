<script>
	let { children } = $props();
	import Navbar from '$lib/nav.svelte';
</script>

<Navbar />

{@render children()}
