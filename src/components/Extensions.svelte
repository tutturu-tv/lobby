<script>
  import ext from '../ext.json'
  const extensions = ext.extensions
</script>

<div class="container">
  <h3>Popular Chrome extensions</h3>
  <div class="list">
    {#each extensions as ex}
      <a href={ex.url} target="_blank" rel="noopener noreferrer">
        <div class="item">
          <img alt={ex.name} class="ext-img" src={ex.icon} width="32" height="32">
          <span>{ex.name}</span>
          <i class="arrow"></i>
        </div>
      </a>
    {/each}
  </div>
  <a href="https://chrome.google.com/webstore/category/extensions" target="_blank" rel="noopener noreferrer">See more</a>
</div>

<style>
  .container {
    background-color: #2e2e2e;
    width: 20.625rem;
    position: absolute;
    right: 0;
    top: 18rem;
    text-align: center;
    padding: 0.625rem 0 1.25rem 0.625rem;
  }
  .list {
    text-align: left;
    margin-bottom: 1.25rem;
  }
  .item {
    position: relative;
    padding: 0.625rem;
    background-color: #212121;
    margin: 0.3125rem 0 0.3125rem 0.3125rem;
    transition: 0.2s background-color ease;
    cursor: pointer;
  }
  .item:hover {
    background-color: #000;
  }
  .ext-img {
    vertical-align: middle;
  }
  a {
    color: #6CB4D2;
  }
  a:active, a:hover {
    text-decoration: none;
  }
  .arrow {
    border: solid #6CB4D2;
    border-width: 0 1px 1px 0;
    display: inline-block;
    padding: 0.3125rem;
    position: absolute;
    right: 1.25rem;
    top: 1.25rem;
    transform: rotate(-45deg);
    -webkit-transform: rotate(-45deg);
  }
</style>
