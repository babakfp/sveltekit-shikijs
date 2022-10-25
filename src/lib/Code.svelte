<script>
	import { getHighlighter, setCDN } from 'shiki'
	setCDN('https://unpkg.com/shiki/')

	export let lang = 'js'
	export let theme = 'nord'

	export let input = `console.log('Hello, World!')`
	let code = 'Loading...'

	$: {
		getHighlighter({ theme, langs: [lang] }).then((highlighter) => {
			code = highlighter.codeToHtml(input, lang, theme)
		}).catch(err => {
			console.log(err)
		})
	}
</script>

<div>
	{@html code}
</div>

<style>
	div :global(pre) {
		padding: 1.5rem;
		border-radius: 6px;
	}
</style>
