<script lang="ts">
	import About from '$lib/components/section/About.svelte';
	import Contact from '$lib/components/section/Contact.svelte';
	import Experience from '$lib/components/section/Experience.svelte';
	import Gallery from '$lib/components/section/Gallery.svelte';
	import Hero from '$lib/components/section/Hero.svelte';
	import Testimonials from '$lib/components/section/Testimonials.svelte';
	import Work from '$lib/components/section/Work.svelte';
	import HeroImage from '$lib/images/home.png';

	// vars
	let pageTitle = 'Dr. Nidhi Sharma - Experienced and Compassionate Gynecologist and Obstetrician';
	let pageDescription =
		'Welcome to the website of Dr. Sharma, a highly skilled and experienced gynecologist and obstetrician who is dedicated to providing the highest quality care to her patients.';
	let ogImage = HeroImage;
	let ogUrl = 'https://nidhisharma.medicreatives.net/';
	let twitterHandle = '@NidhiSh65788564';
	const keywords = "gynecologist, obstetrician, experienced doctor, compassionate care, women's health, Chandigarh, reproductive health, prenatal care, childbirth, fertility, menopause, gynecological disorders, pregnancy, postnatal care, pelvic health, family planning"
</script>

<svelte:head>
	<title>{pageTitle}</title>
	<meta name="description" content={pageDescription} />

	<!-- Open Graph Meta Tags -->
	<meta property="og:title" content={pageTitle} />
	<meta property="og:keywords" content={keywords} />
	<meta property="og:description" content={pageDescription} />
	<meta property="og:image" content={ogImage} />
	<meta property="og:url" content={ogUrl} />
	<meta property="og:type" content="website" />

	<!-- Twitter Card Meta Tags -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:site" content={twitterHandle} />
	<meta name="twitter:title" content={pageTitle} />
	<meta name="twitter:description" content={pageDescription} />
	<meta name="twitter:image" content={ogImage} />
	<meta name="twitter:url" content={ogUrl} />

	<!-- Structured Data (JSON-LD) -->
	<!-- Structured Data (JSON-LD) -->
	<script type="application/ld+json">
	  {
		"@context": "https://schema.org",
		"@type": "Person",
		"name": "Dr. Nidhi Sharma",
		"jobTitle": "Experienced and Compassionate Gynecologist and Obstetrician",
		"url": ogUrl,
		"description": pageDescription,
		"image": ogImage,
		"sameAs": [
		  "https://www.linkedin.com/in/nidhi-sharma-9a30841a/",
		  "https://www.facebook.com/profile.php?id=100092379701574",
		  "https://instagram.com/nidhi.sharma1909?igshid=MzRlODBiNWFlZA=="
		]
	  }
	</script>
</svelte:head>

<Hero />
<About />
<Experience />
<Work />
<Gallery />
<Testimonials />
<Contact />
