<script>
	let books = ['Sample Book 1', 'Sample Book 2', 'Sample Book 3'];
	let newBook;

	const addBook = (ev) => {
		if (ev.key === 'Enter') {
			books = [...books, newBook];
			newBook = '';
		}
	};
</script>

<main>
	<label>
		<h4>Add Book</h4>
		<input
			type="text"
			name="newBook"
			id="newBook"
			bind:value={newBook}
			on:keypress={addBook}
		/>
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
	}

	input {
		padding: 5px 10px;
	}

	ul {
		padding: 5px 0;
	}

	li {
		list-style: none;
	}
</style>
