<script>
	import TodoForm from "../components/TodoForm.svelte";
	import {todos} from "../stores/todoStore";
	import Todo from '../components/Todo.svelte';
</script>

<svelte:head>
	<title>To-do app</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<main>
	<h1 class="text-2xl font-bold text-center text-gray-800 md:text-3xl">My Todos</h1>
	<TodoForm />
	{#each $todos as todo}
		<Todo todo={todo} index={todo.id} />
	{/each}
</main>

<style>
</style>
