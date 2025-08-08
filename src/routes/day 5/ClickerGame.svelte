<script>
	import { onMount } from 'svelte';
	import Button from '../../Components/Button.svelte';

	let points = $state(0);
	let clickingpower = $state(1);
	let passiveIncome = $state(0);

	let upgradeClickCost = 10;
	let upgradePassiveCost = 50;

	onMount(() => {
		//
		let passiveTimer = setInterval(() => {
			points += passiveIncome;
		}, 1000);

		return () => clearInterval(passiveTimer);
	});

	function increment() {
		points += clickingpower;
	}

	function upgradeClickingPower(amount) {
		if (points - amount * upgradeClickCost >= 0) {
			points -= amount * upgradeClickCost;
			clickingPower += amount;
		}
	}
	function upgradePassiveIncome(amount) {
		if (points - amount * upgradePassiveCost >= 0) {
			points -= amount * upgradePassiveCost;
			passiveIncome += amount;
		}
	}
</script>

<div
	class="flex h-screen flex-col items-center justify-center bg-gradient-to-b from-blue-100 via-red-100 to-blue-400"
>
	<div>{points}</div>

	<button
		onclick={increment}
		class="h-48 w-48 rounded-full bg-yellow-700 transition-all duration-100 active:scale-110"
	></button>

	<div class="flex w-full border text-center">
		<div class="flex w-1/2 flex-col">
			<div>Click Upgrades</div>
			<Button text={'+1 - $100'} fn={() => upgradeClickingPower(1)} />
			<Button text={'+5 - $500'} fn={() => upgradeClickingPower(5)} />
			<Button text={'+10 - $100'} fn={() => upgradeClickingPower(10)} />
		</div>
		<div class="w-1/2" flex flex-col>
			<div>Passive Upgrades</div>
			<Button text={'+1 - $200'} fn={() => upgradePassiveIncome(1)} />
			<Button text={'+5 - $600'} fn={() => upgradePassiveIncome(6)} />
			<Button text={'+10 - $1000'} fn={() => upgradePassiveIncome(10)} />
		</div>

		<div></div>
	</div>
</div>
