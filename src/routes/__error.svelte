<!-- ERROR PAGE DISPLAYED WHEN ENDPOINTS DONT EXIST -->
<script context="module">
    export const load = ({ error, status }) => {
        return {
            props: {
                title: `${status}: ${error.message}`,
                status: status
            },
        };
    };
</script>

<svelte:head>
    {#if status == 404}
        <title>Page not found</title>
    {:else}
    <title>{title}</title>
    {/if}
    
</svelte:head>

<script>
    export let title;
    export let status;
</script>

{#if status == 404}
<div class="error">
    <div class="text-center">
        <h1 class="text-8xl">404</h1>
        <h1 class="text-2xl">Page not found</h1>
        <button class="btn btn-primary"><a href="/">Return to homepage</a></button>
    </div>

</div>
{:else}
<div class="error">

    <h1>{title}</h1>
    <h1>Something went wrong</h1>
    <button class="btn btn-primary"><a href="/">Return to homepage</a></button>
</div>
{/if}


<style>
    .error {
        height: 100vh;
        display: grid;
        gap: var(--spacing-32);
        place-content: center;
        place-items: center;
        background-image: url('/pic/Telomerer.png');
        color: white;
    }

</style>
