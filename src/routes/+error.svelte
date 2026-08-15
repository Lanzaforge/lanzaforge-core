<script>
    import { page } from '$app/state';

    let status = $state(page.status);
    let attemptedPath = $state(page.url?.pathname || '/');
</script>

<svelte:head>
    <title>{status} Error | lanzoor.dev</title>
</svelte:head>

{#if status === 404}
    <section id="error-404" class="stretched">
        <a class="plain" href="/" onclick={() => history.back()}> {'<-'} Back </a>

        <header>
            <h1>404</h1>

            <div class="separator"></div>

            <h2>Page not found</h2>
        </header>

        <p>
            <b>
                We couldn't find a resource located at
                <span class="col bright green">'{attemptedPath}'</span>.
            </b><br />
            The filename may have changed, or the file may have been moved or removed.
        </p>
    </section>
    <!-- {:else}
    <section class="stretched">
        <h1>{status} - Internal Server Error</h1>
        <p>An unexpected error occurred. Please try again later.</p>
    </section> -->
{/if}

<style lang="css">
    #error-404 {
        background: radial-gradient(circle at 50% 40%, rgba(100, 0, 255, 0.25), transparent), black;
    }

    #error-404 header {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        gap: 1em;
    }

    #error-404 header .separator {
        width: 2px;
        height: 2em;

        background: rgba(255, 255, 255, 0.25);
    }

    #error-404 p {
        text-align: center;
    }
</style>
