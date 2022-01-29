<template>
	<header class="flex justify-between items-center px-8 py-5 z-40 dark:bg-slate-800 dark:text-white" :class="{'sticky -top-0 backdrop-filter backdrop-blur nav-scroll-bg': !overflow, 'fixed w-screen': overflow}">
		<a href="/">
			<img src="../assets/enigma.svg" class="lg:w-auto w-6 select-none dark:hidden" />
			<img src="../assets/enigma-dark.svg" class="lg:w-auto w-6 select-none hidden dark:block" />
		</a>
		<ul class="lg:flex hidden gap-6">
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#about`"><li>About</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#prizes`"><li>Prizes</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#rules`"><li>Rules</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#touch`"><li>Get in Touch</li></span>
		</ul>
		<div class="block lg:hidden" @click="overflow = !overflow">
			<!-- Light mode -->
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="dark:hidden" v-if="overflow">
				<path d="M19 6.41L17.59 5L12 10.59L6.41 5L5 6.41L10.59 12L5 17.59L6.41 19L12 13.41L17.59 19L19 17.59L13.41 12L19 6.41Z" fill="black"/>
			</svg>
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="dark:hidden" v-else>
				<path d="M3 6H21V8H3V6ZM3 11H21V13H3V11ZM3 16H21V18H3V16Z" fill="black"/>
			</svg>

			<!-- Dark mode -->
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="hidden dark:block" v-if="overflow">
				<path d="M19 6.41L17.59 5L12 10.59L6.41 5L5 6.41L10.59 12L5 17.59L6.41 19L12 13.41L17.59 19L19 17.59L13.41 12L19 6.41Z" fill="white"/>
			</svg>
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="hidden dark:block" v-else>
				<path d="M3 6H21V8H3V6ZM3 11H21V13H3V11ZM3 16H21V18H3V16Z" fill="white"/>
			</svg>
		</div>
	</header>
	<div class="flex justify-center items-center fixed over-flow backdrop-filter backdrop-blur w-screen text-center z-50" v-if="overflow">
		<div>
			<ul class="flex flex-col gap-12 dark:text-white">
				<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#about`"><li>About</li></span>
				<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#prizes`"><li>Prizes</li></span>
				<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#rules`"><li>Rules</li></span>
				<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#touch`"><li>Get in Touch</li></span>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			overflow: false
		}
	}
}
</script>

<style>
header {
	background: white;
	font-family: 'Montserrat', sans-serif;
}

.over-flow {
	background: rgba(256, 256, 256, 1);
	margin-top: 64px;
	height: calc(100vh - 72px);
}

.nav-scroll-bg {
	background: rgba(256, 256, 256, 1);
}

@media (prefers-color-scheme: dark) {
	.over-flow {
		background: rgb(30, 41, 59);
	}
}
</style>
