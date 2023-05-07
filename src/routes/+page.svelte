<script lang="ts">
	import About from '$lib/components/section/About.svelte';
	import Contact from '$lib/components/section/Contact.svelte';
	import Experience from '$lib/components/section/Experience.svelte';
	import Gallery from '$lib/components/section/Gallery.svelte';
	import Hero from '$lib/components/section/Hero.svelte';
	import Testimonials from '$lib/components/section/Testimonials.svelte';
	import Work from '$lib/components/section/Work.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<Hero />
<About />
<Experience />
<Work />
<Gallery />
<Testimonials />
<Contact />
