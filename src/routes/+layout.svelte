<script lang="ts">
	import '../app.postcss';
	import {life} from "../store"
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';



	let lifeTotal;
    const unsubscribe = life.subscribe((value) => {
		lifeTotal = value;
	});

	function life20() {
		life.set(20);
	}

	function life30() {
		life.set(30);
	}

	function life40() {
		life.set(40);
	}
</script>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<strong class="text-xl uppercase">Set Life Total:</strong>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<button
					class="btn btn-sm variant-filled-secondary border text-black border-black shadow-md shadow-black hover:variant-filled-primary"
					on:click={life20}
					>
					20
				</button>

				<button
				class="btn btn-sm variant-filled-secondary border text-black border-black shadow-md shadow-black hover:variant-filled-primary"
				on:click={life30}
				>
				30
				</button>

				<button
				class="btn btn-sm variant-filled-secondary border text-black border-black shadow-md shadow-black hover:variant-filled-primary"
				on:click={life40}
				>
				40
				</button>
			
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
