<script>
	import Button from '../../Components/Button.svelte';
	import LoadingBar from '../../Components/LoadingBar.svelte';
	import HorseRace from './HorseRace.svelte';
	let progress = $state(10);

	function increment() {
		progress += 10;
		if (progress > 100) {
			progress = 100;
		}
	}
	function unincrement() {
		progress -= 10;
		if (progress < 0) {
			progress = 0;
		}
	}
	function reset() {
		progress = 0;
	}
	// make decrement function with a button along with it
	// make a rest function that resets progress to 0
</script>

<div class="bg-red-500 text-center transition-all duration-1000 hover:bg-blue-500">Transition</div>

<div
	class="m-2 h-10 w-12 border transition-all duration-1000 hover:size-50 hover:bg-orange-500 hover:text-center"
>
	Box 1
</div>
<div class="m-2 h-10 w-12 border transition-all duration-1000 hover:scale-125 hover:bg-blue-500">
	Box 2
</div>
<div
	class="m-2 h-10 w-12 border transition-all duration-1000 hover:translate-x-90 hover:rotate-540 hover:bg-green-500"
>
	Box 3
</div>
<div
	class="m-2 h-10 w-12 border transition-all duration-1000 hover:size-50 hover:bg-red-500 hover:text-center hover:invert"
>
	Box 4
</div>
<HorseRace />
<Button text={'Increment'} fn={increment} />
<Button text={'Deincrement'} fn={unincrement} />
<Button text={'Reset'} fn={reset} />
<LoadingBar color={'bg-red-400'} current={progress} max={100} />
