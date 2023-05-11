<script lang="ts">
	import Button from '$lib/components/ui/Button.svelte';
</script>
<section class="text-gray-600 body-font relative" id="contact">
	<div class="absolute inset-0 bg-gray-300">
		<iframe
			width="100%"
			height="100%"
			frameborder="0"
			marginheight="0"
			marginwidth="0"
			title="map"
			scrolling="no"
			src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3429.9732649706507!2d76.77245887596264!3d30.71915198628825!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390fedd07ef90c87%3A0x45a8ce975f996401!2sDr%20Nidhi%20Sharma!5e0!3m2!1sen!2sin!4v1683769922360!5m2!1sen!2sin"
			style="filter: grayscale(1) contrast(1.2) opacity(0.4);"
		/>
	</div>
	<div class="container px-5 py-24 mx-auto flex">
		<div
			class="lg:w-1/3 md:w-1/2 bg-white rounded-lg p-8 flex flex-col md:ml-auto w-full mt-10 md:mt-0 relative z-10 shadow-md"
		>
			<h2 class="text-gray-900 text-lg mb-1 font-medium title-font">Get in Touch</h2>
			<p class="leading-relaxed mb-5 text-gray-600">
				Reach out to Dr. Sharma for Exceptional Gynecological and Obstetric Care
			</p>
			<div class="relative mb-4">
				<label for="email" class="leading-7 text-sm text-gray-600">Email</label>
				<input
					type="email"
					id="email"
					name="email"
					class="w-full bg-white rounded border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out"
				/>
			</div>
			<div class="relative mb-4">
				<label for="message" class="leading-7 text-sm text-gray-600">Message</label>
				<textarea
					id="message"
					name="message"
					class="w-full bg-white rounded border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-200 h-32 text-base outline-none text-gray-700 py-1 px-3 resize-none leading-6 transition-colors duration-200 ease-in-out"
				/>
			</div>
			<Button text="Contact now" />

			<p class="text-xs text-gray-500 mt-3">
				If you have any questions, concerns, or would like to schedule an appointment, please don't hesitate to reach out. Dr. Sharma is a highly skilled and experienced gynecologist and obstetrician committed to providing personalized and compassionate care to women of all ages.
			</p>
		</div>
	</div>
</section>
