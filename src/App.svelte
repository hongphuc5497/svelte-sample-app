<script>
	let books = ['Sample Book 1', 'Sample Book 2', 'Sample Book 3'];
</script>

<main>
	<label>
    <h4>Add Book</h4>
    <input type="text" name="" id="" />
  </label>
	<h4>My Books</h4>
  <ul>
    {#each books as book}
      <li>{book}</li>
    {/each}
  </ul>
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
