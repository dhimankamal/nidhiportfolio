<script lang="ts">
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';
	import SectionHeader from '../ui/SectionHeader.svelte';

	type List = {
		des: string;
		name: string;
		position: string;
	};

	const list: List[] = [
		{
			des: "I am extremely grateful to Dr. Nidhi Sharma for her expertise and compassionate care throughout my infertility journey. As a desperate couple longing for a child, Dr. Sharma's knowledge in assisted reproductive technology and her personalized approach gave us hope and confidence. Her dedication and commitment to our case resulted in a successful IVF treatment, and now we have a beautiful baby boy in our arms. Thank you, Dr. Sharma, for making our dreams come true.",
			name: 'Sarah Johnson',
			position: ' Marketing Manager'
		},
		{
			des: "I had the privilege of being under the care of Dr. Nidhi Sharma during my high-risk pregnancy, and I can't thank her enough for her exceptional skills and professionalism. Dr. Sharma's expertise in obstetrics and gynecology, combined with her reassuring demeanor, provided me with the confidence and support I needed throughout the journey. She guided me through each step, ensuring the well-being of both me and my baby. I would highly recommend Dr. Sharma to any expectant mother seeking exceptional care.",
			name: 'Emily Thompson',
			position: 'HR Manager'
		},
		{
			des: "Dr. Nidhi Sharma is an incredible infertility specialist who helped us overcome years of struggle to conceive. Her extensive knowledge and experience in the field, coupled with her warm and empathetic approach, made us feel comfortable and understood. Dr. Sharma's dedication and attention to detail were evident in every step of our treatment, and her guidance and support were invaluable. Thanks to her expertise, we are now proud parents of twins. We will forever be grateful to Dr. Sharma for making our dreams come true.",
			name: 'David and Lisa Williams',
			position: 'IT Professionals'
		},
		{
			des: 'Dr. Nidhi Sharma is not only an exceptional surgeon but also a compassionate and caring doctor. I underwent a complex gynecological surgery under her care, and I was amazed by her surgical skills and attention to detail. Dr. Sharma ensured that I was well-informed and comfortable throughout the process, and her post-operative care was exemplary. I would highly recommend Dr. Sharma to anyone in need of gynecological surgery or infertility treatment. Her expertise and genuine concern for her patients are truly commendable.',
			name: 'Jennifer Lewis',
			position: 'Teacher'
		}
	];
</script>

<section class="text-gray-600 body-font bg-slate-50" id="testimonials">
	<div class="container px-5 py-24 mx-auto">
		<div class="text-center pb-4">
			<SectionHeader title="Testimonials" />
		</div>

		{#if browser}
			<Carousel>
				{#each list as { name, position, des }}
					<div class="py-4 px-20 xl:w-1/2 lg:w-3/4 w-full mx-auto text-center">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="currentColor"
							class="inline-block w-8 h-8 text-gray-400 mb-8"
							viewBox="0 0 975.036 975.036"
						>
							<path
								d="M925.036 57.197h-304c-27.6 0-50 22.4-50 50v304c0 27.601 22.4 50 50 50h145.5c-1.9 79.601-20.4 143.3-55.4 191.2-27.6 37.8-69.399 69.1-125.3 93.8-25.7 11.3-36.8 41.7-24.8 67.101l36 76c11.6 24.399 40.3 35.1 65.1 24.399 66.2-28.6 122.101-64.8 167.7-108.8 55.601-53.7 93.7-114.3 114.3-181.9 20.601-67.6 30.9-159.8 30.9-276.8v-239c0-27.599-22.401-50-50-50zM106.036 913.497c65.4-28.5 121-64.699 166.9-108.6 56.1-53.7 94.4-114.1 115-181.2 20.6-67.1 30.899-159.6 30.899-277.5v-239c0-27.6-22.399-50-50-50h-304c-27.6 0-50 22.4-50 50v304c0 27.601 22.4 50 50 50h145.5c-1.9 79.601-20.4 143.3-55.4 191.2-27.6 37.8-69.4 69.1-125.3 93.8-25.7 11.3-36.8 41.7-24.8 67.101l35.9 75.8c11.601 24.399 40.501 35.2 65.301 24.399z"
							/>
						</svg>
						<p class="leading-relaxed text-lg">
							{des}.
						</p>
						<span class="inline-block h-1 w-10 rounded bg-blue-500 mt-8 mb-6" />
						<h2 class="text-gray-900 font-medium title-font tracking-wider text-sm">
							{name}
						</h2>
						<p class="text-gray-500">{position}</p>
					</div>
				{/each}
			</Carousel>
		{/if}
	</div>
</section>
