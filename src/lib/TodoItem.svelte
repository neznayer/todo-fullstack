<div class="todo done">
	<form action="" method="">
		<input type="hidden" name="done" id="" />
		<button aria-label="Mark done / not done" class="toggle" />
	</form>

	<form action="" method="" class="text">
		<input type="text" name="" id="" />
		<button aria-label="save todo" class="save">Save</button>
	</form>

	<form action="" method="">
		<button aria-label="Delete this todo" class="delete" />
	</form>
</div>

<style>
	.todo {
		display: grid;
		grid-template-columns: 2rem 1fr 2rem;
		column-gap: 0.5rem;
		align-items: center;
		margin: 0 0 0.5rem 0;
		padding: 0.5rem;
		background-color: white;
		border-radius: var(--border-radius);
		filter: drop-shadow(2px 4px 6px var(--color-shadow));
		transform: translate(-1px, -1px);
		transition: filter 0.2s, transform 0.2s;
	}

	.todo button {
		width: 2rem;
		height: 2rem;
		border: none;
		background-color: transparent;
		background-position: 50% 50%;
		background-repeat: no-repeat;
	}

	.todo input {
		flex: 1;
		padding: 0.5em 2em 0.5em 0.8em;
		border-radius: 0.3rem;
	}
	button.toggle {
		border: 1px solid rgba(0, 0, 0, 0.2);
		border-radius: 50%;
		box-sizing: border-box;
		background-size: 1em auto;
	}

	.text {
		position: relative;
		display: flex;
		align-items: center;
		flex: 1;
	}

	.save {
		position: absolute;
		right: 0.5rem;
		opacity: 0;
		border-radius: 0.3rem;
		font-size: 0.8rem;
		cursor: pointer;
	}

	.todo input:focus + .save,
	.save:focus {
		transition: opacity 0.2s;
		opacity: 1;
		background-color: var(--color-primary);
		width: auto;
	}

	.delete {
		background-image: url("data:image/svg+xml,%3Csvg width='24' height='24' viewBox='0 0 24 24' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M4.5 5V22H19.5V5H4.5Z' fill='%23676778' stroke='%23676778' stroke-width='1.5' stroke-linejoin='round'/%3E%3Cpath d='M10 10V16.5' stroke='white' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'/%3E%3Cpath d='M14 10V16.5' stroke='white' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'/%3E%3Cpath d='M2 5H22' stroke='%23676778' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'/%3E%3Cpath d='M8 5L9.6445 2H14.3885L16 5H8Z' fill='%23676778' stroke='%23676778' stroke-width='1.5' stroke-linejoin='round'/%3E%3C/svg%3E%0A");
		opacity: 0.2;
	}
	.delete:hover,
	.delete:focus {
		transition: opacity 0.2s;
		opacity: 1;
		cursor: pointer;
	}

	/* TODO uncomment when API is ready */

	/* .done {
		opacity: 0.4;
		filter: drop-shadow(0 0 1px var(--color-shadow));
	}

	.done .toggle {
		cursor: pointer;
		background-image: url("data:image/svg+xml,%3Csvg width='22' height='16' viewBox='0 0 22 16' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M20.5 1.5L7.4375 14.5L1.5 8.5909' stroke='%23676778' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E");
	} */
</style>
