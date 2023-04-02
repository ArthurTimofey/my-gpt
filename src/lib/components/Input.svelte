<script lang="ts">
	export let value = '';
	export let placeholder = '';
	export let id = '';
	export let label = '';
	export let type: 'text' | 'email' | 'password' | 'number' | 'tel' | 'url' = 'text';
	export let disabled = false;
	export let required = false;
</script>

<div class="form-control w-full max-w-md">
	<label for="{id}" class="label font-medium pb-1">
		<span class="">{label}</span>
	</label>
	<input
		type="{type}"
		placeholder="{placeholder}"
		name="{id}"
		id="{id}"
		value="{value}"
		class="input input-bordered w-full max-w-lg"
		disabled="{disabled}"
		required="{required}"
	/>
</div>
