<script lang="ts">
    import TopPanel from '$lib/components/Panels/TopPanel.svelte';
    import '../app.css';

    let { children } = $props();
</script>

<TopPanel />

<main>
    {@render children()}
</main>
