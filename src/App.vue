<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Header from './components/Header.vue';
import Footer from './components/Footer.vue'
</script>

<template>
	<Header />

	<!-- Landing -->
	<div class="flex flex-col-reverse gap-12 lg:gap-0 lg:flex-row lg:justify-between justify-center items-center landing home dark:bg-slate-900 dark:text-white">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-5">
			<h1 class="lg:text-5xl text-2xl font-bold">Enigma</h1>
			<h2 class="lg:text-2xl text-xl">Code Wars 0: Battleships</h2>
			<h3 class="lg:text-xl text-lg font-thin">Fight your battles with artillery and code</h3>
			<h2 class="lg:text-2xl text-xl">Feb 3 - Feb 10</h2>
			<br>
			<a href="https://github.com/MU-Enigma/BattleShip-BattleGround/tree/master/Battleship/Submissions">
				<div class="lg:p-6 p-2 lg:w-60 w-32 flex justify-center uppercase lg:text-2xl text-sm items-center lg:rounded-3xl rounded-xl text-white button cursor-pointer transform hover:scale-95 ease-in-out duration-300 shadow-md">
					Submit entry
				</div>
			</a>
		</div>
		<img src="./assets/landing_bin.svg" class="w-4/5 lg:w-2/5 lg:mr-32 select-none" />
	</div>

	<!-- About -->
	<div id="about" class="min-h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center dark:bg-slate-800 dark:text-white">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-8 my-24">
			<h1 class="lg:text-5xl text-2xl font-bold">Overview</h1>
			<h3 class="lg:text-2xl text-lg font-thin">
				A bot-coding tournament for all students of Mahindra University based on the game of <a href="https://en.wikipedia.org/wiki/Battleship_(game)" class="underline">Battleship</a>. 
				Participating teams are required to write a Python code to compete against other teams. 
				The code with the most elegant solution and intelligent solution would win. 
				It’s a battle of Algorithms and Logic!
			</h3>
		</div>
	</div>

	<!-- Prizes -->
	<div id="prizes" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center landing dark:bg-slate-900 dark:text-white">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-8">
			<h1 class="lg:text-5xl text-2xl font-bold">Prizes</h1>
			<h3 class="lg:text-xl text-lg font-thin flex flex-col">
				<span class="pb-4">Cash prizes will be transferred via UPI to the wallets of respective winners. <br>
					In case the recipients do not have UPI wallets, an alternative would be arranged.</span>
				<span>All certificates will be signed by Dr. Prafulla, the Club’s mentor</span><hr class="my-4 dark:border-slate-800">
				<span>Winner: <span class="font-bold">₹4500</span> + First place certificate</span><hr class="my-4 dark:border-slate-800">
				<span>Second place: <span class="font-bold">₹3000</span> + Second place certificate</span><hr class="my-4 dark:border-slate-800">
				<span>Third place: <span class="font-bold">₹2500</span> + Third place certificate</span>
			</h3>
		</div>
	</div>

	<!-- FAQ -->
	<div id="rules" class="min-h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center dark:bg-slate-800 dark:text-white">
		<div class="lg:mx-52 mx-8 flex flex-col gap-2 lg:gap-8 my-40">
			<h1 class="lg:text-5xl text-2xl font-bold">How to Play</h1>
			<ol class="flex flex-col gap-7 text-lg font-thin list-decimal ml-6 lg:ml-12"> 
				<li>Every team is required to submit a single python file</li>
				<li>
					The program should have a <span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">class BattleShip</span> with the following member variables
					<ul class="list-disc ml-5 leading-10">
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">team_name: str</span> - Name of your team</li>
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">board : list(int)</span> - 2D list indicating the position of your ships</li>
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">opponent_board</span> : list(int) - 2D list for tracking enemy ships</li>
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">info : int</span> - Contains details about your attack</li>
					</ul>
				</li>
				<li>
					Member Functions:
					<ul class="flex flex-col gap-4 list-disc ml-5 mt-3">
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">set_board(self)</span> - Returns your 2D list of your ship</li>
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">attack(self)</span> - Return a tuple of two integers. The two integers denotes the position of the board where you want to shoot.</li>
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">hit_or_miss(self, x, y , info)</span> - Doesn't return anything <br>
								x and y is the co-ordinate at which you hit the enemy board. <span class="font-bold">info</span> contains information about the state of your attack.
								<ul class="list-disc ml-5">
									<li>If info = 1 , it means you have missed your shot</li>
									<li>If info = 0 , it means you have hit an enemy ship</li>
									<li>If info = -1 , it means you have attempted to shoot at a place outside the dimensions of the enemy board</li>
									<li>If info = 2, it means you have availed <span class="font-bold">Nullify</span> special Shot (More on Special Shot later)</li>
									<li>If info = 3, it means you have availed <span class="font-bold">Missile Hawkeye Special Move</span>!</li>
								</ul>
						</li>
					</ul>
				</li>
				<li>You may create additional member variables/global variables and functions. But the `above member functions/variables are neccesary` without which you are disqualified and your opponent gets a walk-over</li>
				<li>You are not allowed to import any third party libraries or import from the main game file. You can only use libraries found in Vanilla Python.</li>
				<li>
					Special Moves:<br>
					In your opponent's board, two randomly selected tile/co-ordinates will be assigned with special spot. The special spot are always in one of the ships. So, when you hit this special part of the ship, you get to use one of the following special moves:
					<ul class="flex flex-col gap-4 list-disc ml-5 mt-3">
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">Nullify</span> : Pretty Self Explanatory. It nullifies your opponent's next chance and hence gives you double hit.</li>
						<li><span class="font-bold bg-slate-100 dark:bg-slate-900 py-1 px-2 rounded-lg">Missile Hawkeye</span> : When you activate missile hawkeye, the next time you hit any co-ordinate say (x,y) , you get to eliminate the entire row and column.</li>
						Note : When you activate missile Hawkeye, the very next move is treated as your special attack.
					</ul>
				</li>
				<li>The board is a 2D matrix of 1s and 0s<br>
						How to Set Up Board :
						<ul class="flex flex-col gap-4 list-disc ml-5 mt-3">
							<li>There are 5 ships. One of size 3, two of size 4, and two of size 5.</li>
							<li>The presence of a ship is determined by the ship arrays you have to input. So,<br>
								<code class="block whitespace-pre bg-slate-100 dark:bg-slate-900 rounded-2xl p-3 mt-4">
									board = [<br>
											[3, 3, 3, 1],<br>
											[4, 3, 4, 0],<br>
											[5, 8, 4, 0]<br>
											[1, 1, 5, 1]<br>
											[9, 1, 5, 1]
									]<br>
								</code><br>
								means there are 5 ships.<br>
								The first two parameters represent the row and column numbers, respectively.<br>
								The third parameter represents the size of the ship.<br>
								Lastly, the last parameter represents the orientation of the ship, 0 is for vertical and 1 is for horizontal.


							</li>
							<li>
								The ships cannot be placed diagonally, but can be placed horizontally and Vertically only. Note that the ships cannot overlap!
								<code class="block whitespace-pre bg-slate-100 dark:bg-slate-900 rounded-2xl p-3 mt-4">
									board = [<br>
											[1, 0, 3, 0],<br>
											[5, 2, 4, 0],<br>
											[6, 4, 4, 1]<br>
											[4, 4, 5, 1]<br>
											[0, 1, 5, 1]<br>
									]<br><br>
									OR<br><br>
									board = [<br>
											[1,0,0],<br>
											[0,0,1],<br>
											[1,0,0]<br>
									]<br>
								</code><br>
								are not a valid ship position of a ship!
							</li>
						</ul>
				</li>
				<li>The following link redirects you to a <a href="https://github.com/MU-Enigma/BattleShip-BattleGround/blob/master/Battleship/example_submission/team1.py" class="underline">sample code</a> that every team is expected to submit.
						You may use the same as a boiler plate for your code submission.</li>
				<li>Know more about the classic <a href="https://www.youtube.com/watch?v=RY4nAyRgkLo" class="underline">BattleShip Game</a>.</li>
			</ol>
		</div>
	</div>

	<!-- Get in touch -->
	<div id="touch" class="h-screen flex flex-col-reverse lg:flex-row lg:justify-between justify-center items-center landing dark:bg-slate-900 dark:text-white">
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
@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;700&display=swap');

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
	height: calc(100vh - 64px);
}

@media (prefers-color-scheme: dark) {
	* {
		scrollbar-color: rgb(30, 41, 59) rgb(18, 26, 45);
	}

	body {
		background: rgb(15, 23, 42);
	}

	::-webkit-scrollbar {
		width: 8px;
		background: rgb(18, 26, 45);
	}

	::-webkit-scrollbar-thumb {
			background: rgb(30, 41, 59);
	}
}
</style>
