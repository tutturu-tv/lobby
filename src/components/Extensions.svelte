<script>
    import ext from '../ext.json'
    const extensions = ext.extensions
</script>

<div class="spacer">
    <h3>Popular Chrome extensions</h3>
    <div class="grid">
        {#each extensions as ex}
            <a href={ex.url}>
                <div class="grid-item">
                    <img alt={ex.name} class="ext-img" src={ex.icon} width="32" height="32">
                    <span>{ex.name}</span>
                </div>
            </a>
        {/each}
    </div>
    <a href="https://chrome.google.com/webstore/category/extensions">see more</a>
</div>

<style>
    .spacer {
        margin-top: 70px;
    }
    .grid {
        margin: 30px 0;
        width: 780px;
        display: grid;
        grid-template-columns: auto auto auto;
    }
    .grid-item {
        padding: 10px;
        background-color: #f3f3f3;
        transition: 0.2s background-color ease;
        cursor: pointer;
    }
    .grid-item:hover {
        background-color: #dedede;
    }
    .ext-img {
        vertical-align: middle;
    }
</style>
