<script lang="ts">
    import FooterPanel from '$lib/components/Panels/FooterPanel.svelte';
    import TopPanel from '$lib/components/Panels/TopPanel.svelte';
    import '../app.css';

    let { children } = $props();
</script>

<TopPanel />

<main>
    {@render children()}
</main>

<FooterPanel />
