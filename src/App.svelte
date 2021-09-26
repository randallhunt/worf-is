<script>
	let adjective = '';
	let noun = '';
	let article = 'a';
	generate();

	function generate() {
		adjective = genAdjective();
		noun = genNoun();
		article = 'aeiou'.indexOf(adjective.charAt(0)) > -1 ? 'an' : 'a';
	}
	function genAdjective() {
		const adjectives = [
			'bad', 'terrible', 'lousy', 'no good', 'weak', 'lame', 'worthless',
			'good', 'wonderful', 'great', 'awesome', 'amazing',
			'ugly', 'hungry', 'scruffy-looking', 'stargazing',
			'insecure', 'horny', 'sexy', 'petulent', 'leaping', 'sex-starved',
			'unfaithful', 'long-haired', 'bionic'
		];
		const index = Math.floor(Math.random() * adjectives.length);
		return adjectives[index];
	}
	function genNoun() {
		const nouns = [
			'actor', 'father', 'son', 'husband', 'klingon', 'security officer',
			'lieutenant', 'pilot', 'painter', 'tribble', 'shape-shifter',
			'engineer', 'beast', 'sex partner', 'mechanic', 'pilates instructor',
			'yoga teacher', 'rocket launcher', 'dream', 'nightmare',
			'baseball player', 'runningback', 'goalkeeper', 'dancer',
			'singer', 'lover', 'joker', 'winner', 'loser'
		];
		const index = Math.floor(Math.random() * nouns.length);
		return nouns[index];
	}
</script>

<main>
	<h1>Worf is {article} {adjective} {noun}</h1>
	<p>&nbsp;</p>
	<p><button on:click={generate}>Try again</button></p>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>