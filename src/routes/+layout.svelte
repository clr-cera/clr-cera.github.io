<script>
	import '../app.css';

	let { children } = $props();

	import Navbar from '$lib/nav.svelte';
</script>

<div class="font-mono">
	<Navbar />

	{@render children()}
</div>
