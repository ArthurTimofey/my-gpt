<script lang="ts">
	let messages: string[] = [];

	function handleSubmit(e: Event) {
		e.preventDefault();
		// get form chatInput value from Event
		const chatInput = (e.target as HTMLFormElement).chatInput.value;
		messages = [...messages, chatInput];
	}
</script>

<div class="h-screen flex flex-col">
	<div class="bg-gray-50 flex-grow border-x">
		{#if messages.length > 0}
			<ul>
				{#each messages as message}
					<li>{message}</li>
				{/each}
			</ul>
		{:else}
			<p>No messages yet.</p>
		{/if}
	</div>
	<form on:submit="{handleSubmit}">
		<div class="flex">
			<div class="form-control flex-grow">
				<textarea
					id="chatInput"
					name="chatInput"
					class="border-x border-t resize-none h-96 outline-none"
					placeholder="Write to god"></textarea>
			</div>
			<button type="submit" class="border-r border-y">Send</button>
		</div>
	</form>
</div>
