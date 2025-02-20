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
		<h2 class="text-2xl font-bold mb-4">Sposób z with - prostszy i bezpieczniejszy!</h2>
		<Code
		  bind:this={code}
		  lang="python"
		  theme="github-dark"
		  code={`
	# Ten sam efekt, ale prościej i bezpieczniej:
	with open("dane.txt", "r") as plik:
		tekst = plik.read()
	# Python automatycznie zamknie plik po zakończeniu!
		  `}
		  options={{
			showAll: false
		  }}
		/>
	  </div>
	</div>
	
	<Action do={() => showLines('1-2')} />
	<Action do={() => showLines('1-3')} />
	<Action do={() => showLines('*')} />