<script lang="ts">
	export let data;
</script>

<div class="flex flex-col items-center h-full w-full">
	{#if !data.user}
		not logged in
	{:else}
		logged in
	{/if}
</div>
