<template>
	<div>
		<header-element></header-element>

		<!-- Side elements -->
		<side-element>
			<div class="w-full h-full flex justify-center items-center flex-col">
				<a href="#main_section">
					<i class="fa-regular fa-square iconSection" :class="{'font-bold': CURRENT_PAGE == 0}"></i>
				</a>
				<a href="#about_section">
					<i class="fa-regular fa-square iconSection" :class="{'font-bold': CURRENT_PAGE == 1}"></i>
				</a>
				<a href="#technology_section">
					<i class="fa-regular fa-square iconSection" :class="{'font-bold': CURRENT_PAGE == 2}"></i>
				</a>
				<a href="#portfolio_section">
					<i class="fa-regular fa-square iconSection" :class="{'font-bold': CURRENT_PAGE == 3}"></i>
				</a>
				<a href="#contact_section">
					<i class="fa-regular fa-square iconSection" :class="{'font-bold': CURRENT_PAGE == 4}"></i>
				</a>
			</div>
		</side-element>
		<side-element right>
			<div class="flex flex-col justify-center items-center h-full w-full">
				<div class="h-2/3 w-full flex">
					<div class="w-1/2 h-full border-r border-stone-300"></div>
					<div class="w-1/2 h-full"></div>
				</div>
				<div class="h-1/3 w-full flex justify-center items-center">
					<p class="whitespace-nowrap rotate-90 text-stone-400">Made by Narei ©2022</p>
				</div>
			</div>
		</side-element>

		<!-- Main content -->
		<div class="w-full h-full flex flex-col justify-center items-center">

			<!-- Main section -->
			<section-element id="main_section">
				<template v-slot:header>01. Main section</template>
				<template v-slot:content>
					<div class="w-full flex justify-center flex-col items-center">
						<p class="text-sm md:text-lg text-stone-400">
							# narei.dev
						</p>
						<h1 class="font-bold text-xl md:text-2xl">
							Olaf
							<span class="text-2xl md:text-3xl border-b-2 border-stone-400">`Narei`</span>
							Król
						</h1>
						<p class="mt-2 text-stone-400 text-center text-sm md:text-md">
							Ambitious junior front-end developer!
							<br>
							<span class="text-stone-400 text-xs md:text-sm">Scroll or click `Explore more`...</span>
						</p>
					</div>
					<div class="mt-16 text-center">
						<button class="btn" @click="scrollToPage(1)">Explore more  
							<i class="fa-solid fa-arrow-right text-stone-100"></i>
						</button>
					</div>
				</template>
			</section-element>

			<!-- About section -->
			<section-element id="about_section">
				<template v-slot:header>02. About me</template>
				<template v-slot:content>
					<div class="w-full h-full flex flex-col justify-between">
						<div class="w-full text-xs md:text-sm">
							<h6 class="mb-4">Hi! Thanks for visiting my site! I'm a 18 year old front-end developer, based in Poznań, Poland.</h6>
							<p class="mb-4">
								My name is Olaf and I'm self-learning JavaScript developer for 7 months. 
								I'm mostly interested in vue.js, but I would like to get to know as many technologies as possible. 
								I have been learning programming for 5 years. Initially I was coding simple applications and REST APIs in Java, but 
								I find web development more interesting.
							</p>
							<p>I'm open to new opportunities and continuous self development.</p>
						</div>
						<div class="w-full flex justify-end">
							<button class="btn">
								Download CV
								<i class="fa-regular fa-file text-stone-100"></i>
							</button>
						</div>
					</div>
				</template>
			</section-element>

			<!-- Technology section -->
			<section-element id="technology_section">
				<template v-slot:header>03. Technologies and skills</template>
				<template v-slot:content>
					<div class="w-full grid grid-cols-3 md:grid-cols-4 gap-y-12">
						<technology-element name="vue js" stars=4>
							<i class="fa-brands fa-vuejs"></i>
						</technology-element>
						<technology-element name="javascript" stars=4>
							<i class="fa-brands fa-square-js"></i>
						</technology-element>
						<technology-element name="node js" stars=2>
							<i class="fa-brands fa-node-js"></i>
						</technology-element>
						<technology-element name="java" stars=2>
							<i class="fa-brands fa-java"></i>
						</technology-element>
						<technology-element name="html" stars=5>
							<i class="fa-brands fa-html5"></i>
						</technology-element>
						<technology-element name="css" stars=4>
							<i class="fa-brands fa-css3-alt"></i>
						</technology-element>
						<technology-element name="bootstrap" stars=3>
							<i class="fa-brands fa-bootstrap"></i>
						</technology-element>
						<technology-element name="tailwind" stars=3>
							<img src="@/assets/tailwindcss-icon.svg" alt="Tailwind" width="38">
						</technology-element>
					</div>
					<div class="w-full mt-8 hidden md:block">
						I'm learning to become professional frontend developer but backend concepts are no strange to me.
						I was using bootstrap or my own styles before but recently I started styling my sites using tailwind-css.
						I'm open to learning new technologies and adapt the tools used to the wishes of clients.
					</div>
				</template>
			</section-element>

			<!-- Portfolio section -->
			<section-element id="portfolio_section">
				<template v-slot:header>04. My work</template>
				<template v-slot:content>
					<div class="w-full h-full flex flex-col">
						<p class="text-xs md:text-sm mb-4">
							I use github as a platform to publish my work. Click the button to check all my projects.
						</p>

						<div class="grid grid-cols-1 divide-y divide-stone-300">
							<div class="py-1">
								<span class="font-bold">To Do application </span>
								<a class="text-stone-500" href="https://github.com/iEranDEV/ToDo-application">(click)</a>
							</div>
							<div class="py-1">
								<span class="font-bold">Weather application </span>
								<a class="text-stone-500" href="https://github.com/iEranDEV/WeatherApp">(click)</a>
							</div>
							<div class="py-1">
								<span class="font-bold">Visual memory game </span>
								<a class="text-stone-500" href="https://github.com/iEranDEV/VisualMemory">(click)</a>
							</div>
						</div>
						<div class="w-full flex justify-end mt-4">
							<button class="btn">
								Check more on github
								<i class="fa-brands fa-github text-stone-100"></i>
							</button>
						</div>
					</div>
				</template>
			</section-element>

			<!-- Contact section -->
			<section-element id="contact_section">
				<template v-slot:header>05. Contact me</template>
				<template v-slot:content>
					<div class="w-full h-full flex flex-col">
						<form ref="form" @submit.prevent="sendEmail">
							<div class="w-full flex flex-col items-center px-2">
								<div class="w-full xl:w-1/2">
									<label for="email" class="text-stone-400">enter your name</label>
									<input type="email" name="email" id="email" class="input" placeholder="example@gmail.com">
								</div>
								<div class="w-full xl:w-1/2 mt-8 mb-8">
									<label for="message" class="text-stone-400">enter your message</label>
									<textarea name="message" id="message" cols="30" rows="8" class="input" placeholder="message..."></textarea>
								</div>
							</div>
							<div class="w-full flex justify-end">
								<button class="btn" type="submit">
									Send message 
									<i class="fa-regular fa-envelope text-stone-100"></i>
								</button>
							</div>
						</form>
					</div>
				</template>
			</section-element>
		</div>

		<notification-element :positive="positiveNotification"></notification-element>
	</div>
</template>

<script>
import HeaderElement from '@/components/static/HeaderElement.vue'
import SideElement from '@/components/static/SideElement.vue'
import SectionElement from '@/components/SectionElement.vue'
import TechnologyElement from '@/components/TechnologyElement.vue'
import NotificationElement from '@/components/static/NotificationElement.vue'

import { ref } from 'vue';
import emailjs from '@emailjs/browser';

export default {
	setup() {
	
		const PAGES = ['main_section', 'about_section', 'technology_section', 'portfolio_section', 'contact_section'];
		let CURRENT_PAGE = ref(0);
		let TIMEOUT = true;

		document.addEventListener('wheel', (e) => {
			e.preventDefault();

			if(TIMEOUT) {
				TIMEOUT = false;
				if(e.wheelDeltaY > 0) {
					if(CURRENT_PAGE.value != 0) {
						let element = document.getElementById(PAGES[CURRENT_PAGE.value - 1]);
						CURRENT_PAGE.value -= 1;
						window.scrollTo(0, element.offsetTop)
					}
				} else {
					if(CURRENT_PAGE.value != 4) {
						let element = document.getElementById(PAGES[CURRENT_PAGE.value + 1]);
						CURRENT_PAGE.value += 1;
						window.scrollTo(0, element.offsetTop)
					}
				}

				setTimeout(() => {
					TIMEOUT = true;
				}, 500)
			}

		}, { passive: false });

		return {
			CURRENT_PAGE,
			PAGES,
		}
	},
	data() {
		return {
			positiveNotification: true,
		}
	},
	methods: {
		scrollToPage(id) {
			let element = document.getElementById(this.PAGES[id]);
			this.CURRENT_PAGE = id;
			element.scrollIntoView();
		},
		sendEmail() {
			emailjs.sendForm('service_lgpm9cr', 'template_gupbsq5', this.$refs.form, 'FkmGARS4SLBYangHK')
				.then(() => {
					this.positiveNotification = true;
					let notification = document.getElementById('notification');
					if(notification.classList.contains('hidden')) {
						notification.classList.remove('hidden');
						notification.classList.add('flex');
					}
					setTimeout(() => {
						notification.classList.remove('flex');
						notification.classList.add('hidden');
					}, 3000)
				}, () => {
					this.positiveNotification = false;
					let notification = document.getElementById('notification');
					if(notification.classList.contains('hidden')) {
						notification.classList.remove('hidden');
						notification.classList.add('flex');
					}
					setTimeout(() => {
						notification.classList.remove('flex');
						notification.classList.add('hidden');
					}, 3000)
				});
			document.getElementById('email').value = '';
			document.getElementById('message').value = '';
		}
	},
	components: {
		HeaderElement,
		SideElement,
		SectionElement,
		TechnologyElement,
		NotificationElement
	}
}
</script>

<style>

</style>
