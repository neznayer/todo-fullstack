<script>
	import TodoItem from '$lib/TodoItem.svelte';

	const title = 'Todos';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<div class="todos">
	<h1>{title}</h1>
	<form action="" method="" class="new">
		<input type="text" name="text" id="todo" placeholder="Add a todo" />
	</form>

	<TodoItem />
	<TodoItem />
	<TodoItem />
</div>

<style>
	.todos {
		width: 100%;
		max-width: 42rem;
		margin: 4rem auto 0 auto;
	}
	.new {
		margin: 0;
		margin-bottom: 0.5rem;
	}

	.todos :global(input) {
		border: none;
		box-sizing: border-box;
		border-radius: var(--border-radius);
		border: 1px solid transparent;
		text-align: center;
		outline: none;
	}

	.new input {
		font-size: 2.8rem;
		padding: 0.5em 1em;
		background-color: transparent;
		width: 100%;
	}

	.todos :global(input:focus-visible) {
		box-shadow: inset 1px 1px 6px var(--color-shadow);
		border: 1px solid var(--color-accent);
		outline: none;
		box-sizing: border-box;
	}
</style>
