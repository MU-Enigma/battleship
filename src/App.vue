<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Header from './components/Header.vue';
import Footer from './components/Footer.vue'
</script>

<template>
	<Header />
	<div class="flex flex-col-reverse gap-12 lg:gap-0 lg:flex-row lg:justify-between justify-center items-center landing home min-h-screen">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-5">
			<h1 class="lg:text-5xl text-2xl font-bold">Enigma</h1>
			<h2 class="lg:text-3xl text-xl">Battleship Challenge</h2>
			<h3 class="lg:text-2xl text-lg font-thin">Fight your battles with artillery and code</h3>
			<h2 class="lg:text-3xl text-xl">Jan 30 - Feb 6</h2>
			<br>
			<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">
				<div class="lg:p-6 p-2 lg:w-60 w-32 flex justify-center uppercase lg:text-2xl text-sm items-center lg:rounded-3xl rounded-xl text-white button cursor-pointer transform hover:scale-95 ease-in-out duration-300 shadow-md">
					Submit entry
				</div>
			</a>
		</div>
		<img src="./assets/landing_bin.svg" class="w-4/5 lg:w-2/5 lg:mr-32 select-none" />
	</div>

	<div id="about" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-8">
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
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-8">
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

	<div id="rules" class="min-h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-8 my-24">
			<h1 class="lg:text-5xl text-2xl font-bold">Tournament rules</h1>
			<ol class="lg:text-base text-lg font-thin flex flex-col list-decimal gap-4 ml-6 lg:ml-12"> 
				<li>Every team is required to submit a single python file</li>
				<li>
					The program should have a `class BattleShip` with the following member variables
					<ul class="list-disc">
						<li><span class="font-bold">team_name: str</span> - Name of your team</li>
						<li><span class="font-bold">board : list(int)</span> - 2D list indicating the position of your ships</li>
						<li><span class="font-bold">opponent_board</span> : list(int) - 2D list for tracking enemy ships</li>
						<li><span class="font-bold">info : int</span> - Contains details about your attack</li>
					</ul>
				</li>
				<li>
					Member Functions:
					<ul class="list-disc">
						<li><span class="font-bold">set_board(self)</span> - Returns your 2D list of your ship</li>
						<li><span class="font-bold">attack(self)</span> - Return a tuple of two integers. The two integers denotes the position of the board where you want to shoot.</li>
						<li><span class="font-bold">hit_or_miss(self, x, y , info)</span> - Doesn't return anything.
								x and y is the co-ordinate at which you hit the enemy board. `info` contains information about the state of your attack.
								* If info = 1 , it means you have missed your shot.
								* If info = 0 , it means you have hit an enemy ship
								* If info = -1 , it means you have attempted to shoot at a place outside the dimensions of the enemy board
								* If info = 2, it means you have availed `Nullify` special Shot (More on Special Shot later)
								* If info = 3, it means you have availed `Missile Hawkeye Special Move`!</li>
					</ul>
				</li>
				<li>You may create additional member variables/global variables and functions. But the `above member functions/variables are neccesary` without which you are disqualified and your opponent gets a walk-over</li>
				<li>You are not allowed to import any third party libraries or import from the main game file. You can only use libraries found in Vanilla Python.</li>
				<li>
					Special Moves:<br>
					In your opponent's board, two randomly selected tile/co-ordinates will be assigned with special spot. The special spot are always in one of the ships. So, when you hit this special part of the ship, you get to use one of the following special moves:
					<ul class="list-disc">
						<li><span class="font-bold">Nullify</span> : Pretty Self Explanatory. It nullifies your opponent's next chance and hence gives you double hit.</li>
						<li><span class="font-bold">Missile Hawkeye</span> : When you activate missile hawkeye, the next time you hit any co-ordinate say (x,y) , you get to eliminate the entire row and column.</li>
						Note : When you activate missile Hawkeye, the very next move is treated as your special attack.
					</ul>
				</li>
				<li>The board dimensions are 10x10.</li>
				<li>The following link redirects you to a <a href="https://github.com/MU-Enigma/BattleShip-BattleGround/blob/master/Battleship/example_submission/team1.py" class="underline">sample code</a> that every team is expected to submit.
						You may use the same as a boiler plate for your code submission.</li>
				<li>Know more about the classic <a href="https://www.youtube.com/watch?v=RY4nAyRgkLo" class="underline">BattleShip Game</a>.</li>
			</ol>
		</div>
	</div>

	<div id="touch" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center landing">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-8">
			<h1 class="lg:text-5xl text-2xl font-bold">Get in Touch</h1>
			<h2 class="lg:text-2xl text-lg font-thin flex flex-col">
				Got questions?<br>
				Join our discord server and we'll be right with you.
			</h2>
			<br>
			<a href="https://discord.gg/5eJwmkV">
				<div class="p-6 w-60 flex justify-center items-center rounded-3xl text-white button cursor-pointer transform hover:scale-95 ease-in-out duration-300 shadow-md">
					<img src="./assets/Discord-Logo+Wordmark-White.svg" >
				</div>
			</a>
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
