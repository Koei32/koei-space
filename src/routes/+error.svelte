<script lang="ts">
    import { page } from "$app/state";
</script>

<div class="error">
    <h2>{page.status}</h2>
    <h3>{page.error?.message}</h3>
</div>

<svelte:head>
    <title>done messed up</title>
</svelte:head>

<style>
    * {
        font-family: "IBM Plex Mono";
        color: white;
        font-weight: 300;
        margin: 0;
        padding: 0;
    }

    div {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>
