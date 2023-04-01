<script lang="ts">
	export let value = '';
	export let placeholder = '';
	export let id = '';
	export let label = '';
	export let type: 'text' | 'email' | 'password' | 'number' | 'tel' | 'url' = 'text';
	export let disabled = false;
	export let required = false;
</script>

<div class="form-control">
	<label for={id} class="">
		<span class="">{label}</span>
	</label>
	<input
		{type}
		{placeholder}
		name={id}
		{id}
		{value}
		class="border-black border-2 p-1 rounded"
		{disabled}
		{required}
	/>
</div>
