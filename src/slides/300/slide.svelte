<script>
	import { Code, Action } from '@animotion/core'
	
	let modernCode;
	</script>
	
	<div class="grid h-full place-content-center place-items-center">
	  <div class="w-full max-w-3xl bg-white/5 rounded-xl p-6">
		<h2 class="text-3xl font-bold mb-4">Sposób 2: Nowoczesny (z with)</h2>
		<Code
		  bind:this={modernCode}
		  lang="python"
		  theme="github-dark"
		  code={`
	# Krócej i bezpieczniej!
	with open("notatki.txt", "r") as plik:
		tekst = plik.read()
	# Plik zostanie automatycznie zamknięty!
		  `}
		/>
	  </div>
	</div>
	
	<Action do={() => modernCode.selectLines`2`} />
	<Action do={() => modernCode.selectLines`3`} />
	<Action do={() => modernCode.selectLines`4`} />