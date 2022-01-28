<template>
	<header class="flex justify-between items-center px-8 py-5 z-40" :class="{'sticky -top-0 backdrop-filter backdrop-blur nav-scroll-bg': !overflow, 'fixed w-screen': overflow}">
		<a href="/">
			<img src="../assets/enigma.svg" class="lg:w-auto w-6 select-none" />
		</a>
		<ul class="lg:flex hidden gap-6">
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#about`"><li>About</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#prizes`"><li>Prizes</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#rules`"><li>Rules</li></span>
			<span class="hover:underline transition ease-in-out duration-300 cursor-pointer" v-scroll-to="`#touch`"><li>Get in Touch</li></span>
		</ul>
		<div class="block lg:hidden" @click="overflow = !overflow">
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M3 6H21V8H3V6ZM3 11H21V13H3V11ZM3 16H21V18H3V16Z" fill="black"/>
			</svg>
		</div>
	</header>
	<div class="flex justify-center items-center fixed over-flow backdrop-filter backdrop-blur w-screen text-center z-50" v-if="overflow">
		<div>
			<ul class="flex flex-col gap-12">
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
</style>
