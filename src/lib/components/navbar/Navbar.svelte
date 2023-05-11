<script lang="ts">
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';

	import Hamburger from '../svg/icons/Hamburger.svelte';
	import Logo from '../svg/icons/Logo.svelte';
	import Button from '../ui/Button.svelte';
	import { navlinks } from './navlinks';

	let isActive: boolean = false;
	let activeSectionId: string | null = null;

	const handleMenuClick = () => (isActive = !isActive);

	onMount(() => {
		const observer = new IntersectionObserver((entries) => {
			entries.forEach((entry) => {
				const { isIntersecting, target } = entry;
				const sectionId = target.id;

				if (isIntersecting) {
					// Section entered the viewport
					if (sectionId !== activeSectionId) {
						// Update active section
						activeSectionId = sectionId;
					}
				} else {
					// Section left the viewport
					if (sectionId === activeSectionId) {
						// Update active section
						activeSectionId = null;
					}
				}
			});
		});

		// Get all sections by their IDs
		const sections = Array.from(document.querySelectorAll('section'));

		// Observe each section
		sections.forEach((section) => {
			observer.observe(section);
		});
	});

	$: console.log('activeSectionId', activeSectionId);
</script>

<header class="text-gray-600 body-font sticky top-0 bg-white z-50">
	<div
		class="container mx-auto flex flex-wrap px-5 py-2 md:py-4 flex-row md:flex-row items-center justify-between"
	>
		<a
			href="/"
			class="flex title-font font-medium items-center justify-center text-gray-900 md:mb-0"
		>
			<Logo />
		</a>
		<div class="items-center hidden md:flex">
			<nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
				{#each navlinks as { title, href }}
					<a
						{href}
						class:text-blue-500={href === '#' + activeSectionId}
						class="mr-5 hover:text-gray-900">{title}</a
					>
				{/each}
			</nav>
			<Button text="Contact us" href="#contact" varient={activeSectionId === "contact"?"primary":"secondary"} size="sm" />
		</div>
		<div class="md:hidden">
			<button on:click={handleMenuClick}><Hamburger bind:isActive /></button>
		</div>
	</div>
</header>

<!-- mobile menu -->
{#if isActive}
	<div transition:fade class="sticky top-0 h-screen w-screen bg-slate-50 flex items-center justify-center z-20">
		<nav class="flex flex-col w-full p-4 space-y-4">
			{#each navlinks as { title, href }}
				<a {href} on:click={handleMenuClick} class="mr-5 text-2xl hover:text-gray-900">{title}</a>
			{/each}
		</nav>
	</div>
{/if}
