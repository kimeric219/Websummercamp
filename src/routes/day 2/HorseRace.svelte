<!-- HorseRace.svelte -->
<script>
	import Horse from './Horse.svelte';
	import Button from '../../Components/Button.svelte';

	let horses = $state([
		{
			emote: '🐎',
			position: 0,
			color: 'bg-gradient-to-r from-red-400 via-red-300 to-red-200',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-gradient-to-b from-blue-400 via-blue-300 to-blue-200',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-gradient-to-r from-yellow-400 via-yellow-300 to-yellow-200',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-gradient-to-r from-orange-400 via-orange-300 to-orange-200',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-gradient-to-r from-green-400 via-green-300 to-green-200',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-gradient-to-r from-red-400 via-red-300 to-red-200',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-gradient-to-r from-blue-400 via-blue-300 to-blue-200',
			animation: 'bounce'
		}
	]);

	function progress() {
		let maxHorse = horses[0];
		for (let horse of horses) {
			let r = parseInt(Math.random() * 20);
			horse.position += r;
			if (horse.position > 100) {
				horse.position = 100;
			}
			if (horse.position > maxHorse.position) {
				maxHorse = horse;
			}
		}

		for (let horse of horses) {
			if (horse.position == maxHorse.position) {
				horse.animation = 'spin';
			} else {
				horse.animation = 'bounce';
			}
		}
	}
	function reset() {
		let maxHorse = horses[0];
		for (let horse of horses) {
			let r = parseInt(Math.random() * 20);
			horse.position = 0;
			horse.animation = 'bounce';
		}
	}
</script>

<div style="height: 600px;" class="bg-green-500">
	<div class="py-5 text-center text-2xl font-bold">HORSE RACING GAME</div>
	<Button text={'Progress'} fn={progress} />
	<Button text={'Reset'} fn={reset} />
	<div class="py-10 pr-10">
		{#each horses as horse}
			<Horse
				emote={horse.emote}
				color={horse.color}
				animation={horse.animation}
				position={horse.position}
			/>
		{/each}
	</div>
</div>
