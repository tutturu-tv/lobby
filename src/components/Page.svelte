<script>
  import Tutturu from './Tutturu.svelte'
  import SearchSign from './SearchSign.svelte'
  import Highlight from './Highlight.svelte'
  import Extensions from './Extensions.svelte'
  import Discord from './Discord.svelte'

  export let sub
  export let a
</script>

<div class="site">
  <SearchSign />
  <main class="box">
    <Tutturu />
    <Highlight sub={sub} a={a} />
  </main>
  <Discord />
  <Extensions />
</div>

<style>
  .site {
    font-family: 'Montserrat', sans-serif;
  }

  .box {
    text-align: center;
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -40%);
  }
</style>
