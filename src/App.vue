<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Header from './components/Header.vue';
import Footer from './components/Footer.vue'
</script>

<template>
	<Header />
	<div class="flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center landing home">
		<div class="mx-52 flex flex-col gap-2 lg:gap-5">
			<h1 class="lg:text-5xl text-2xl font-bold">Enigma</h1>
			<h2 class="lg:text-3xl text-xl">Battleship Challenge</h2>
			<h3 class="lg:text-2xl text-lg font-thin">Fight your battles with artillery and code</h3>
			<h2 class="lg:text-3xl text-xl">Jan 30 - Feb 6</h2>
		</div>
		<img src="./assets/landing_bin.svg" class="w-0 lg:w-2/5 mr-32 select-none" />
	</div>

	<div id="about" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center">
		<div class="mx-52 flex flex-col gap-2 lg:gap-8">
			<h1 class="lg:text-5xl text-2xl font-bold">Overview</h1>
			<h3 class="lg:text-2xl text-lg font-thin">
				A bot-coding tournament for all students of Mahindra University based on the game of <a href="https://en.wikipedia.org/wiki/Battleship_(game)" class="underline">Battleship</a>. 
				Participating teams are required to write a Python code to compete against other teams. 
				The code with the most elegant solution and intelligent solution would win. 
				It’s a battle of Algorithms and Logic!
			</h3>
		</div>
	</div>

	<div id="prizes" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center landing">
		<div class="mx-52 flex flex-col gap-2 lg:gap-8">
			<h1 class="lg:text-5xl text-2xl font-bold">Prizes</h1>
			<h3 class="lg:text-xl text-lg font-thin flex flex-col">
				<span class="pb-4">Cash prizes will be transferred via UPI to the wallets of respective winners. <br>
					In case the recipients do not have UPI wallets, an alternative would be arranged.</span>
				<span>All certificates will be signed by Prafulla ma'am, the Club’s mentor</span><hr class="my-4">
				<span>Winner: <span class="font-bold">₹4500</span> + First place certificate</span><hr class="my-4">
				<span>Second place: <span class="font-bold">₹3000</span> + Second place certificate</span><hr class="my-4">
				<span>Third place: <span class="font-bold">₹2500</span> + Third place certificate</span>
			</h3>
		</div>
	</div>

	<div id="rules" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center">
		<div class="mx-52 flex flex-col gap-2 lg:gap-8">
			<h1 class="lg:text-5xl text-2xl font-bold">Tournament rules</h1>
			<ol class="lg:text-2xl text-lg font-thin flex flex-col list-decimal gap-4 ml-12"> 
				<li>Submission: Fixed size, no folders</li>
				<li>Programming language to use Python3+ (without external libraries)</li>
				<li>Team size: (1-5), People who have no team can join the team-making program.</li>
				<li>
					Game specifications:
					<ul class="list-disc">
						<li>Time limit: If you pass the time limit of x milliseconds your disqualified.</li>
						<li>Board size: 10 x 10 grid</li>
						<li>Special moves are applicable</li>
					</ul>
				</li>
			</ol>
		</div>
	</div>

	<div id="touch" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center landing">
		<div class="mx-52 flex flex-col gap-2 lg:gap-8">
			<h1 class="lg:text-5xl text-2xl font-bold">Get in Touch</h1>
			<h2 class="lg:text-2xl text-lg font-thin flex flex-col">
				Got questions?<br>
				Join our discord server and we'll be right with you.
			</h2>
			<div class="p-6 w-52 flex justify-center items-center rounded-3xl text-white button font-sans text-xl cursor-pointer transform hover:scale-95 ease-in-out duration-300 shadow-md"><a href="https://discord.gg/5eJwmkV">Engima Discord</a></div>
		</div>
	</div>

	<Footer />
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');

body {
	margin: 0;
}

#app {
	font-family: 'Roboto Mono', monospace;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: black;
}

.landing {
	background: #f2f4f8;
}

.button {
	background-color: #5865F2;
}

.home {
	height: calc(100vh - 72px);
}
</style>
