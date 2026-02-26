<script lang="ts">
    import svelte88x31 from "$lib/assets/svelte88x31.png";
    import github88x31 from "$lib/assets/github88x31.png";
    import discord88x31 from "$lib/assets/discord88x31.png";
    function copyDiscord() {
        navigator.clipboard.writeText("koei32");
    }
    let props = $props();
</script>

<div class="footer-wrapper">
    <div class="socials">
        <a href="https://github.com/Koei32">
            <img src={github88x31} alt="github" /></a
        >
        <a onclick={copyDiscord} aria-label="discord" href="/"
            ><img src={discord88x31} alt="discord" /></a
        >
        <!-- <ul>
            <li><a href="https://github.com/Koei32">GitHub</a></li>
        </ul>
        <a target="_blank" href="https://github.com/Koei32" aria-label="github"
            ><i class="fa-brands fa-github"></i></a
        >
        <a target="_blank" href="/">test</a>
        <a target="_blank" href="/">test</a>
        <a target="_blank" href="/">test</a> -->
    </div>
    <div class="end">
        <p>Thanks for visiting!</p>
        <div class="buttons">
            <a href="https://svelte.dev/"
                ><img src={svelte88x31} alt="svelte" /></a
            >
        </div>
    </div>
</div>

<style>
    .footer-wrapper {
        background-color: var(--bg-color-sec);
        width: auto;
        height: auto;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 15px;
        color: var(--fg-color);
        border-top: 1px #5f5f5f solid;
    }

    a {
        margin-right: 5px;
    }

    .socials {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .end {
        width: 40%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: end;
    }

    p {
        font-size: 12px;
        font-family: var(--pri-font);
    }

    .buttons {
        margin-top: 10px;
        display: flex;
    }
</style>
