<div class="relative h-screen overflow-hidden bg-gradient-to-b from-black via-purple-900 to-black">
	<div class="absolute top-1/2 left-1/2 h-8 w-8 -translate-1/2 rounded-full bg-yellow-200"></div>

	<!--- mercury -->
	<div
		class="absolute top-1/2 left-1/2 h-12 w-12 -translate-1/2 animate-[spin_8s_linear_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-2 w-2 translate-0.5 rounded-full bg-gray-400"></div>
	</div>
	<!--- venus -->
	<div
		class="absolute top-1/2 left-1/2 h-24 w-24 -translate-1/2 animate-[spin_12s_linear_infinite] rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-2 w-2 translate-2.5 rounded-full bg-gradient-to-b from-red-400 via-red-300 to-orange-200"
		></div>
	</div>
	<!--- earth -->
	<div
		class="absolute top-1/2 left-1/2 h-36 w-36 -translate-1/2 animate-[spin_16s_linear_infinite] rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-2 w-2 translate-4 animate-[spin_8s_linear_infinite] rounded-full bg-gradient-to-b from-blue-300 via-blue-400 to-green-300"
		>
			<div class="h-1 w-1 -translate-[4px] rounded-full bg-white"></div>
		</div>
		<!--- mars -->
		<div
			class="absolute top-1/2 left-1/2 h-48 w-48 -translate-1/2 animate-[spin_24s_linear_infinite] rounded-full border border-gray-200/40"
		>
			<div class="absolute h-2 w-2 translate-6 rounded-full bg-green-400"></div>
		</div>
		<!--- Jupiter -->
		<div
			class="absolute top-1/2 left-1/2 h-60 w-60 -translate-1/2 animate-[spin_32s_linear_infinite] rounded-full border border-gray-200/40"
		>
			<div
				class="absolute h-2 w-2 translate-7.5 rounded-full bg-gradient-to-b from-orange-300 via-green-300 to-orange-400"
			></div>
			<!--- Saturn -->
			<div
				class="absolute top-1/2 left-1/2 h-72 w-72 -translate-1/2 animate-[spin_40s_linear_infinite] rounded-full border border-gray-200/40"
			>
				<div class="absolute h-2 w-2 translate-9 rounded-full bg-green-200"></div>
			</div>
			<!--- Uranus -->
			<div
				class="absolute top-1/2 left-1/2 h-84 w-84 -translate-1/2 animate-[spin_48s_linear_infinite] rounded-full border border-gray-200/40"
			>
				<div class="absolute h-2 w-2 translate-11 rounded-full bg-blue-200"></div>
			</div>
			<!--- Neptune -->
			<div
				class="absolute top-1/2 left-1/2 h-96 w-96 -translate-1/2 animate-[spin_56s_linear_infinite] rounded-full border border-gray-200/40"
			>
				<div class="absolute h-2 w-2 translate-13 rounded-full bg-blue-500"></div>
			</div>
		</div>
	</div>

	<!-- stars -->
	{#each Array(100) as _, i}
		<div
			class="absolute h-0.5 w-0.5 animate-pulse rounded-full bg-white/60"
			style="top: {Math.random() * 90}vh; left:{Math.random() * 90}vw "
		></div>
	{/each}
</div>
