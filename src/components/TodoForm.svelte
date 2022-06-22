<script>
    import {addTodo} from "../stores/todoStore"

    let todo = '';

    const handleSubmit = () => {
        addTodo(todo);
        todo = '';
        console.log('submiting')
    }
 </script>


<form class="my-6" on:submit|preventDefault={handleSubmit}>
	<div class="flex flex-col text-sm mb-2">
		<label class="font-bold mb-2 text-gray-800" for="todo" />
		<input
			type="text"
			name="todo"
			placeholder="watcha gotta do?"
			class="apparance-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500 rounded-lg"
            bind:value={todo}
		/>
	</div>
	<button type="submit" class="w-full shadow-sm rounded bg-blue-300 hover:bg-blue-400 text-gray-600 py-2 px-4">Submit</button>
</form>
