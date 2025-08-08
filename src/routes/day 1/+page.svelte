<script>
	import Button from '../../Components/Button.svelte';
</script>

<div class="w-full bg-cyan-300">
	<div class="prose p-5">
		<h1 class="text-center">Eric's Profile</h1>

		<hr />

		<div class="profile-image h-20 w-20 overflow-hidden rounded-full bg-black bg-cover bg-center">
			>
		</div>
		<div>Eric Kim</div>
		<div>Programmer</div>

		<h2 class="text-center">About Me</h2>

		<p class="text-center">Hi my name is Eric.</p>

		<h2 class="text-center">Haiku Exercise</h2>
		<h4 class="bg-blue-400 text-center">the sun pours herself</h4>
		<h4 class="bg-green-400 text-center">into the sea and the world</h4>
		<h4 class="bg-blue-100 text-center">overflows with light</h4>

		<h2 class="text-center">Components</h2>

		<Button text={'CLICK ME'} message={'I was clicked'} />
		<Button text={"DON'T CLICK ME"} message={'Why did you click me?'} />
	</div>
</div>

<style>
	.profile-image {
		background-image: url('https://images.unsplash.com/photo-1635686692794-b0ce6337386b?q=80&w=735&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
	}
</style>
