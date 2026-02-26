<script lang="ts">
    import Footer from "$lib/components/footer.svelte";
    import Navbar from "$lib/components/navbar.svelte";
    import { titles } from "$lib/titles";
    let title = titles[Math.floor(Math.random() * titles.length)];
</script>

<svelte:head>
    <title>koei.space - {title}</title>
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
