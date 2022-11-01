<script>
	import TodoItem from '$lib/TodoItem.svelte';

	const title = 'Todos';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<h1>{title}</h1>
<form action="" method="">
	<input type="text" name="text" id="todo" placeholder="Add a todo" />
</form>

<TodoItem />
