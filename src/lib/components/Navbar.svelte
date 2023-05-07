<script lang="ts">
	import Button from '$lib/ui/Button.svelte';

	const navlinks = [
		{
			title: 'Home',
			href: '/'
		},
		{
			title: 'About us',
			href: '#about'
		},
		{
			title: 'Experience',
			href: '#experience'
		},
		{
			title: 'Work',
			href: '#work'
		},
		{
			title: 'Gallery',
			href: '#gallery'
		},
		{
			title: 'Testimonials',
			href: '#testimonials'
		}

		
	];
</script>

<header class="text-gray-600 body-font sticky top-0 bg-white">
	<div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
		<a href="/" class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				stroke="currentColor"
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-width="2"
				class="w-10 h-10 text-white p-2 bg-blue-500 rounded-full"
				viewBox="0 0 24 24"
			>
				<path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5" />
			</svg>
			<span class="ml-3 text-xl" />
		</a>
		<nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
			{#each navlinks as { title, href }}
				<a {href} class="mr-5 hover:text-gray-900">{title}</a>
			{/each}
		</nav>
		<Button href="#contact" text="Contact us" varient="secondary" size="sm" />
	</div>
</header>
