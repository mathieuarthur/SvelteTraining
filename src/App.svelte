<script>
	import Paragraph from './svelte/paragraph.svelte';

	let name = 'world';
	let src = '/img/bongo.gif';
	let gifName = 'Bongo';
	let testText = `Eh oh c'est le truc <strong> de ouf </strong>`;
	let count = 0;

	function handleClick()
	{
		count += 1;
	}
	
</script>

<style>
	p {
		color:navajowhite;
		font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
		text-align: center;
	}
</style>

<input bind:value={name}>

<h1>Hello {name.toUpperCase()}!</h1>

<p> Est-ce que c'est un P ?</p>

<Paragraph/>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>{@html testText}</p>



<img {src} alt="{gifName}">