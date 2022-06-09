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
    <title>{status}</title>
</svelte:head>

<script>
    export let title;
    export let status;
</script>

{#if status == 404}
<div class="error">

    <h1>{title}</h1>
    <h1>The requested resource is not found</h1>
    <button class="btn btn-primary"><a href="/">Return to homepage</a></button>
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
