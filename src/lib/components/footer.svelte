<script lang="ts">
    import svelte88x31 from "$lib/assets/svelte88x31.png";
    import github88x31 from "$lib/assets/github88x31.png";
    import discord88x31 from "$lib/assets/discord88x31.png";
    import koeispace from "$lib/assets/koeispace.gif";

    let showCopyBubble = $state(false);
    let discordCopied = $state(false);

    function copyDiscord() {
        navigator.clipboard.writeText("koei32");
        discordCopied = true;
    }

    // function showCopyBubble() {
    //     showCopyBubble = true;
    // }
    let props = $props();
</script>

<div class="footer-wrapper">
    <div class="socials">
        <a target="_blank" href="https://github.com/Koei32" class="button8831">
            <img src={github88x31} alt="github" /></a
        >
        <div class="discord-wrapper button8831">
            {#if showCopyBubble}
                <span>{discordCopied ? "copied!" : "click to copy"}</span>
            {/if}
            <a
                onclick={copyDiscord}
                onmouseover={() => (showCopyBubble = true)}
                onmouseleave={() => {
                    showCopyBubble = false;
                    discordCopied = false;
                }}
                onfocus={() => (showCopyBubble = true)}
                aria-label="discord"
                href="/"
            >
                <img src={discord88x31} alt="discord" /></a
            >
        </div>
    </div>
    <div class="end">
        <!-- <p>Thanks for visiting!</p> -->
        <a href="https://koei.space/" class="koeispace"
            ><img src={koeispace} alt="koeispace" /></a
        >
    </div>
</div>

<style>
    .koeispace {
        height: 32px;
        line-height: 0;
        border: 1px grey solid;
    }

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

    .button8831 {
        margin-right: 5px;
        height: 31px;
        width: 88px;
    }

    .koeispace {
        margin: 0;
    }

    span {
        background-color: #00000072;
        width: 100px;
        padding: 7px;
        border-radius: 5px;
        bottom: 60px;
        position: fixed;
        font-size: 0.75em;
        font-family: var(--pri-font);
        text-align: center;
    }

    .socials {
        height: 31px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .end {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>
