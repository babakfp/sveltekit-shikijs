<script>
	import Code from '../lib/Code.svelte'
</script>

<h1 style="text-align: center;">Welcome to SvelteKit + ShikiJS</h1>

<Code />
<Code input={`body { margin: 0 }`} lang="css" />
<Code input={`console.log('Hello, World!')`} lang="js" />
<Code theme="rose-pine" />

<style>
	:global(*) {
		margin: 0;
	}
	:global(body) {
		padding: 1rem;
		background: #222831;
		color: #DDDDDD;
		font-family: monospace;
	}
	h1 {
		margin-bottom: 1rem;
	}

	:global(pre) {
		padding: 0.125rem/* 2px */;
		font-size: 0.875rem/* 14px */;
	  line-height: 1.25rem/* 20px */;
		tab-size: 4;
		box-shadow: inset 0 0 0 1px rgb(255 255 255 / 0.05);
		border-radius: 0.5rem/* 8px */;
	}
	:global(pre code) {
		display: block;
		padding: 1.5rem/* 24px */;
		overflow-x: auto;
		line-height: 1.5rem/* 24px */;
	}
</style>
