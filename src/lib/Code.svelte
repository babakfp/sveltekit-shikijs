<script>
	import { getHighlighter } from 'shiki'
	export let lang = 'js'
	export let theme = 'nord'
	export let input = `<h1>Hello, World!</h1>`
</script>

{#await getHighlighter({ theme, langs: [lang] })}
	<p>Waiting...</p>
{:then highlighter}
	{@html highlighter.codeToHtml(input, lang, theme)}
{:catch error}
	<p>{error.message}</p>
{/await}
