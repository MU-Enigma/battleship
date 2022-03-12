<template>
	<header class="flex justify-between items-center px-8 py-5 z-40 sticky -top-0 dark:bg-slate-800/60 dark:text-white" :class="{'backdrop-filter backdrop-blur': !overflow, 'fixed w-screen': overflow}">
		<a href="/">
			<img src="../assets/enigma.svg" class="lg:w-auto w-6 select-none dark:hidden" />
			<img src="../assets/enigma-dark.svg" class="lg:w-auto w-6 select-none hidden dark:block" />
		</a>
		<ul class="lg:flex hidden gap-6">
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#about`"><li>About</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#prizes`"><li>Prizes</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#rules`"><li>FAQ</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#touch`"><li>Get in Touch</li></span>
		</ul>
		<div class="block lg:hidden" @click="overflow = true">
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
	<div class="fixed z-50 inset-0 lg:hidden" v-if="overflow">
		<div class="fixed inset-0 bg-black/20 backdrop-blur-sm" @click="overflow = false"></div>
		<div class="fixed top-4 right-4 w-full max-w-xs bg-slate-900 rounded-lg shadow-lg p-6 text-base font-semibold">
			<button @click="overflow = false" class="absolute top-5 right-5 w-8 h-8 flex items-center justify-center text-slate-500 hover:text-slate-600">
				<svg viewBox="0 0 10 10" class="w-2.5 h-2.5 overflow-visible" aria-hidden="true">
					<path d="M0 0L10 10M10 0L0 10" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"></path>
				</svg>
			</button>
			<ul class="flex flex-col gap-12 text-black dark:text-white">
				<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#about`"><li>About</li></span>
				<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#prizes`"><li>Prizes</li></span>
				<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#rules`"><li>FAQ</li></span>
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
	font-family: 'Montserrat', sans-serif;
}

.over-flow {
	background: rgba(256, 256, 256, 0.6);
	margin-top: 64px;
	height: calc(100vh - 64px);
}

@media (prefers-color-scheme: dark) {
	.over-flow {
		background: rgb(30, 41, 59);
	}
}
</style>
