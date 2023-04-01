<script lang="ts">
	import { Input } from '$lib/components';

	export let data;

	console.log(data);
</script>

<div class="flex flex-col items-center h-full w-full">
	{#if !data.user}
		<h2 class="mt-2 text-center text-3xl font-bold tracking-thight text-base-content">Login</h2>

		<form action="?/login" method="" class="flex flex-col items-center space-y-2 w-full pt-4">
			<div class="form-control w-full max-w-md">
				<label class="font-medium pb-1" for="email">
					<span>Email</span>
				</label>
				<input type="email" name="email" class="input input-bordered w-full max-w-md" />
			</div>

			<div class="form-control w-full max-w-md">
				<label class="font-medium pb-1" for="password">
					<span>Password</span>
				</label>
				<input type="password" name="password" class="input input-bordered w-full max-w-md" />
			</div>

			<div class="w-full max-w-md pt-2">
				<button type="submit" class="btn btn-primary w-full">Login</button>
			</div>
		</form>
	{:else}
		logged in
	{/if}
</div>
