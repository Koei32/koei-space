<script lang="ts">
    import Footer from "$lib/components/footer.svelte";
    import Navbar from "$lib/components/navbar.svelte";
</script>

<svelte:head>
    <title>is for koei</title>
</svelte:head>

<div class="wrapper">
    <Navbar />
    <Footer />
</div>

<style>
    .wrapper {
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
</style>
