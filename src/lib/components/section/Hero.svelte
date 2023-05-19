<script>
	import Button from '$lib/components/ui/Button.svelte';
	import HeroImage from '$lib/images/home.png';
</script>

<section class="text-gray-600 body-font">
	<div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
		<div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
			<img
				class="object-cover object-center rounded"
				alt="hero"
				src={HeroImage}
			/>
		</div>
		<div
			class="lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
		>
			<h1 class="title-font sm:text-6xl font-bold text-3xl mb-4 text-gray-900">
				Dr. Nidhi Sharma
			</h1>
			<p class="title-font sm:text-xl text-2xl mb-4 font-medium text-gray-900">
				- Experienced and Compassionate Gynecologist and Obstetrician
			</p>
			<p class="mb-8 leading-relaxed">
				Welcome to the website of Dr. Sharma, a highly skilled and experienced gynecologist and
				obstetrician who is dedicated to providing the highest quality care to her patients. With
				extensive experience in ultrasound, obstetric and gynecological surgery, and assisted
				reproduction, Dr. Sharma has helped countless women achieve optimal reproductive health and
				overcome a wide range of gynecological and obstetric issues.
			</p>
			<div class="flex justify-center gap-4">
				<Button text="contact" href="#contact" />
				<Button text="about" href="#about" varient="secondary" />
			</div>
		</div>
		
	</div>
</section>
