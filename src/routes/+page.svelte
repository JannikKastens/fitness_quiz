<script>
	let question = 'Wie viele Kalorien verbrennt man beim Joggen?';
	let options = ['100', '200', '300', '400'];
	let answer = '';

	function checkAnswer() {
		if (answer === '300') {
			alert('Richtig! Du verbrennst etwa 300 Kalorien beim Joggen.');
		} else {
			alert('Leider falsch. Die richtige Antwort ist 300 Kalorien.');
		}
	}
</script>

<main>
	<h1>Fitness Quiz</h1>
	<h2>{question}</h2>

	{#each options as option}
		<label>
			<input type="radio" bind:group={answer} value={option} />
			{option}
		</label>
	{/each}

	<button on:click={checkAnswer}>Antwort überprüfen</button>
</main>

<style>
	main {
		text-align: center;
		margin-top: 50px;
	}

	h1 {
		font-size: 24px;
		margin-bottom: 20px;
	}

	h2 {
		font-size: 18px;
		margin-bottom: 10px;
	}

	label {
		display: block;
		margin-bottom: 10px;
	}

	button {
		margin-top: 20px;
		padding: 10px 20px;
		background-color: #007bff;
		color: #fff;
		border: none;
		border-radius: 4px;
		cursor: pointer;
	}
</style>
