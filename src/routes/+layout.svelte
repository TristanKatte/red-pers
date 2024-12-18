<script>
	import Geometric from '../lib/Organism/geometricTransition.svelte'
    import { onNavigate } from '$app/navigation';

onNavigate((navigation) => {
	if (!document.startViewTransition) return;

	return new Promise((resolve) => {
		document.startViewTransition(async () => {
			resolve();
			await navigation.complete;
		});
	});
});
</script>

<link rel="stylesheet" href="/global.css">


<Geometric />
<slot></slot>
