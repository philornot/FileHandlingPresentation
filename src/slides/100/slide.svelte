<script lang="ts">
	import { Code, Action } from '@animotion/core'
	let code: ReturnType<typeof Code>
	
	function showLines(lines: string) {
	  if (code) {
		code.selectLines(lines)
	  }
	}
	</script>
	
	<div class="grid h-full place-content-center place-items-center">
	  <div class="w-full max-w-3xl bg-white/5 rounded-xl p-6">
		<h2 class="text-2xl font-bold mb-4">Sposób tradycyjny</h2>
		<Code
		  bind:this={code}
		  lang="python"
		  theme="github-dark"
		  code={`
	# Krok 1: Otwieramy plik
	plik = open("dane.txt", "r")
	
	# Krok 2: Czytamy zawartość
	tekst = plik.read()
	
	# Krok 3: Zamykamy plik (łatwo o tym zapomnieć!)
	plik.close()
		  `}
		  options={{
			showAll: false
		  }}
		/>
	  </div>
	</div>
	
	<Action do={() => showLines('1-2')} />
	<Action do={() => showLines('1-5')} />
	<Action do={() => showLines('*')} />