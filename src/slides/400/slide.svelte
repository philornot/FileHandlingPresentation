<script>
	import { Code, Action } from '@animotion/core'
	
	let tryCode;
	</script>
	
	<div class="grid h-full place-content-center place-items-center">
	  <div class="w-full max-w-3xl bg-white/5 rounded-xl p-6">
		<h2 class="text-3xl font-bold mb-4">A co jeśli coś pójdzie nie tak?</h2>
		<Code
		  bind:this={tryCode}
		  lang="python"
		  theme="github-dark"
		  code={`
	try:
		with open("nieistniejacy.txt", "r") as plik:
			tekst = plik.read()
	except FileNotFoundError:
		print("Przepraszam, nie mogę znaleźć pliku!")
	except PermissionError:
		print("Nie mam uprawnień do otwarcia pliku!")
		  `}
		/>
	  </div>
	</div>
	
	<Action do={() => tryCode.selectLines`1-3`} />
	<Action do={() => tryCode.selectLines`4-5`} />
	<Action do={() => tryCode.selectLines`6-7`} />