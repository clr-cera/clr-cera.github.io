<script>
	import '../app.css';

	let { children } = $props();

	import Navbar from '$lib/nav.svelte';
</script>

<div class="bg-mybg text-myfg h-screen w-screen rounded-none font-mono">
	<Navbar />
	<div class="m-4">
		{@render children()}
	</div>
</div>
