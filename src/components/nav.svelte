<script>
    let darkMode = true;
    function themeToggle() {
        darkMode = !darkMode;
    }
</script>

<svelte:head>
    {#if !darkMode}
        <link rel="stylesheet" href="light.css">
    {:else}
        <link rel="stylesheet" href="dark.css">
    {/if}
</svelte:head>

<nav>
    <div class="row">
        <div class="col-lg-12" style="display: inline">
            {#if !darkMode}
            <a on:click={themeToggle} style="display: inline">🌞</a>
            {:else}
            <a on:click={themeToggle} style="display: inline">🌜</a>
            {/if}
            <p style="display: inline">
                &nbsp; &nbsp;
                <a>Résumé</a>
            </p>
        </div>
    </div>
    <div class="width-restriction">
    </div>
</nav>

<style>
    nav {
        text-align: right;
        padding-top: 20px;
    }
</style>