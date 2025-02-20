<script>
	import { Code, Action } from '@animotion/core'
	
	let traditionalCode;
	</script>
	
	<div class="grid h-full place-content-center place-items-center">
	  <div class="w-full max-w-3xl bg-white/5 rounded-xl p-6">
		<h2 class="text-3xl font-bold mb-4">Sposób 1: Tradycyjny</h2>
		<Code
		  bind:this={traditionalCode}
		  lang="python"
		  theme="github-dark"
		  code={`
	# Otwieramy plik
	plik = open("notatki.txt", "r")
	
	# Czytamy zawartość
	tekst = plik.read()
	
	# Musimy pamiętać o zamknięciu!
	plik.close()
		  `}
		/>
	  </div>
	</div>
	
	<Action do={() => traditionalCode.selectLines`2`} />
	<Action do={() => traditionalCode.selectLines`5`} />
	<Action do={() => traditionalCode.selectLines`8`} />