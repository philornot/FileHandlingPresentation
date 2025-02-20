<script lang="ts">
	import { Presentation, Slides } from '@animotion/core'
	</script>
	
	<Presentation
	  options={{
		history: true,
		transition: 'slide',
		controls: false,
		progress: true,
		width: 1920,
		height: 1080,
		margin: 0.1,
		center: true,
		transitionSpeed: 'slow',
		backgroundTransition: 'fade',
	  }}
	>
	  <Slides center={true} />
	</Presentation>
	
	<style>
	  :global(.reveal .slides) {
		text-align: left;
	  }
	  
	  :global(.reveal h1) {
		font-size: 3em;
		font-weight: bold;
		letter-spacing: -0.03em;
	  }
	  
	  :global(.reveal h2) {
		font-size: 2.5em;
		font-weight: bold;
		letter-spacing: -0.03em;
	  }
	  
	  :global(.reveal p) {
		font-size: 1.5em;
		line-height: 1.4;
	  }
	
	  :global(.reveal li) {
		font-size: 1.5em;
		line-height: 1.6;
		margin-bottom: 0.5em;
	  }
	
	  :global(.reveal code) {
		font-family: 'Hack', monospace;
		border-radius: 8px;
	  }
	
	  :global(.reveal pre) {
		box-shadow: 0 4px 24px rgba(0,0,0,0.15);
		border-radius: 12px;
	  }
	
	  :global(.reveal .code-wrapper) {
		margin: 2em 0;
	  }
	
	  :global(body) {
		background-color: #111827;
	  }
	</style>