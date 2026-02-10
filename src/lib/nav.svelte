<script>
	import { onMount } from 'svelte';

	onMount(() => {
		const collapseMenu = document.getElementById('MenuLines');
		const collapseBtn = document.getElementById('menubtn');

		if (!collapseMenu || !collapseBtn) {
			console.error('Menu elements not found');
			return;
		}

		collapseBtn.addEventListener('click', () => {
			collapseMenu.classList.toggle('collapse');
		});
	});
</script>

<nav
	class="border-mypurple flex flex-col items-center
  justify-center border-b-1
  px-2
  py-1.5 text-white
  md:flex-row
  "
>
	<div class="flex flex-row">
		<a href="https://github.com/clr-cera">
			<img
				class="max-width-[100px] mx-2 my-1 max-h-[50px] rounded-xl"
				id="footerlogo"
				src="https://avatars.githubusercontent.com/u/93736542?v=4"
				alt="Logo"
			/>
		</a>
		<button id="menubtn" class="collapse-btn text-myorange md:hidden" aria-label="Menu">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke-width="1.5"
				stroke="currentColor"
				class="size-6"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
				/>
			</svg>
		</button>
	</div>
	<div
		id="MenuLines"
		class="text-myorange collapse flex flex-col items-center justify-center p-4 text-xl *:px-3 *:py-2 md:visible md:flex-row"
	>
		<a href="/"><strong>Home</strong></a>
		<a href="/about"><strong>About</strong></a>
		<a href="/blog"><strong>Blog</strong></a>
		<a href="/contact"><strong>Contact</strong></a>
		<a href="/recipes"><strong>Recipes</strong></a>
		<a href="/projects"><strong>Projects</strong></a>
	</div>
</nav>
