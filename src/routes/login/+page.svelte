<script lang="ts">
	import { Input } from '$lib/components';
</script>

<div class="flex flex-col items-center h-full w-full">
	<h2 class="mt-2 text-center text-3xl font-bold tracking-thight text-base-content">Login</h2>

	<form action="?/login" method="POST" class="flex flex-col items-center space-y-2 w-full pt-4">
		<Input id="email" type="email" label="Email" />
		<Input id="password" type="password" label="Password" />
		<div class="w-full max-w-md pt-2">
			<button type="submit" class="btn btn-primary w-full">Login</button>
		</div>
	</form>
</div>
