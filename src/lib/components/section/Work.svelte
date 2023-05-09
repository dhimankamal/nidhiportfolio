<script lang="ts">
	import SectionHeader from '../ui/SectionHeader.svelte';

	type List = {
		title: String;
	};

	const list: List[] = [
		{
			title: `Thesis on “Use of Low Dose Magnesium Therapy in treatment of Ecclampsia”: Completed during post-graduation, this research work explored the efficacy of using low-dose magnesium therapy in treating ecclampsia, a potentially life-threatening complication in pregnant women.`
		},
		{
			title:
				'Paper Presentation on “Programmed Labour” at 48th AICOG 2005: This paper, presented at the 48th All India Congress of Obstetrics and Gynecology in 2005, discussed the concept of programmed labor and its benefits in improving maternal and fetal outcomes.Paper Presentation on “Programmed Labour” at 48th AICOG 2005: This paper, presented at the 48th All India Congress of Obstetrics and Gynecology in 2005, discussed the concept of programmed labor and its benefits in improving maternal and fetal outcomes.'
		},
		{
			title:
				'Paper Presentation on “Stimulation Protocol for IUI in Patients with Hypogonadotropic Hypogonadism” in Fertivision 2008: This paper presented at Fertivision 2008 focused on the stimulation protocol used for intrauterine insemination (IUI) in patients with hypogonadotropic hypogonadism, a condition that affects fertility.'
		},
		{
			title:
				'Paper Presentation on “Efficacy and Safety of Addition of Low Dose Human Chorionic Gonadotropin as Luteal Support in Prevention of OHSS in PCOS Patients” at ISAR 2015: Presented at the Indian Society for Assisted Reproduction (ISAR) 2015 conference in Chennai, this paper evaluated the effectiveness and safety of using low-dose human chorionic gonadotropin (hCG) as luteal support to prevent ovarian hyperstimulation syndrome (OHSS) in polycystic ovary syndrome (PCOS) patients undergoing ovulation induction.'
		},
		{
			title:
				'Invited Faculty Panelist at Fertivision 2015: Invited as a panelist at Fertivision 2015 in New Delhi, the speaker shared insights on the latest advancements in the field of reproductive medicine.'
		},
		{
			title:
				'Hands-On Workshop on 3D/4D USG Usage in OBGY in Ludhiana in March 2014: This workshop, held in Ludhiana in March 2014, provided hands-on training on the use of 3D/4D ultrasound in obstetrics and gynecology.'
		},
		{
			title:
				'5th National Conference of Society of Endoscopic & Laparoscopic Surgeons in India 2012: This conference, held in 2012, brought together leading experts in the field of endoscopic and laparoscopic surgery in India to share their knowledge and expertise.'
		},
		{
			title:
				'Workshop on Endoscopy Organized by FERTICON 2012: This workshop, organized by FERTICON in 2012, focused on the use of endoscopy in reproductive medicine and provided insights on the latest techniques and procedures.'
		},
		{
			title:
				'Annual Conference of Obstetrics & Gynaecological Society of Northern India 2012: Held in 2012, this conference brought together professionals in the field of obstetrics and gynecology to share their research findings, insights, and expertise.'
		},
		{
			title:
				'Workshop on Birth Defects Organized by Department of OBG, PGIMER 2012: This workshop, organized by the Department of Obstetrics and Gynecology at PGIMER in 2012, provided insights on the latest research findings and treatment options for birth defects.'
		},
		{
			title:
				'5th National Conference of Indian Fertility Society 2010: Held in 2010, this conference brought together leading experts in the field of fertility to share their insights and knowledge on the latest research findings and treatment options.'
		},
		{
			title:
				'CME on Labour Room Protocols Organized by FOGSI at GMCH-32 2008: This Continuing Medical Education (CME) program, organized by the Federation of Obstetric and Gynecological Societies of India (FOGSI) at GMCH-32'
		}
	];
</script>

<section class="text-gray-600 body-font bg-slate-50" id="work">
	<div class="container px-5 py-24 mx-auto">
		<div class="text-center mb-20">
			<SectionHeader title="Professional Research and Conference Participation" />
			<p class="text-base leading-relaxed xl:w-2/4 lg:w-3/4 mx-auto">
				Blue bottle crucifix vinyl post-ironic four dollar toast vegan taxidermy. Gastropub indxgo
				juice poutine, ramps microdosing banh mi pug.
			</p>
		</div>
		<div class="flex flex-wrap lg:w-4/5 sm:mx-auto sm:mb-2 -mx-2">
			{#each list as { title }}
				<div class="p-2 w-full">
					<div class="bg-gray-100 rounded flex p-4 h-full items-center">
						<svg
							fill="none"
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="3"
							class="text-blue-500 w-6 h-6 flex-shrink-0 mr-4"
							viewBox="0 0 24 24"
						>
							<path d="M22 11.08V12a10 10 0 11-5.93-9.14" />
							<path d="M22 4L12 14.01l-3-3" />
						</svg>
						<span class="title-font font-medium">{title}</span>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
