<script>
  export let sub
  export let a
  let experiment = a ? 'a' : 'b'
  let usertype = sub ? 'premium' : 'free'
</script>

<div>
  <h2>New Premium Feature!</h2>
  <h2>Save your favorite websites and extensions for next time!</h2>
  {#if a}
    <video id="{usertype}-ad" class="vid" src="/ad.mp4" controls />
  {:else}
    <video preload="auto" class="vid" src="/demo.webm" autoplay muted loop title="Demo" />
  {/if}
  <h3 class="dim">Tired of starting from scratch at the<br />beginning of every session?</h3>
  {#if sub}
    <button id="premium-{experiment}" class="comfy">Show me how!</button>
  {:else}
    <button id="free-{experiment}" class="comfy">Get Premium Now!</button>
  {/if}
</div>

<style>
  .comfy {
    background-color: #627ff1;
    text-shadow: 0 0 1px #eee;
    width: fit-content;
    border-radius: 7.5rem;
    font-size: 16pt;
    font-weight: 600;
    padding: 1.25rem 1.875rem;
    display: inline-block;
    color: white;
    border: 0;
    position: relative;
  }

  @keyframes gg {
    0%,
    10.01%,
    20.01%,
    30.01% {
      transform: scale(1, 1);
      opacity: 1;
    }
    10%,
    20%,
    30%,
    40% {
      transform: scale(1.15, 1.45);
      opacity: 0;
    }
  }

  .comfy::before {
    content: '';
    position: absolute;
    top: -1px;
    left: -1px;
    display: block;
    width: 100%;
    height: 100%;
    border: 1px solid white;
    border-radius: 7.5rem;
    animation: gg 10s infinite;
    animation-delay: 1s;
    pointer-events: none;
    opacity: 0;
  }

  .vid {
    width: 45rem;
  }

  .dim {
    color: #a1a7aa;
  }

  .comfy:hover {
    background-color: #7a92f3;
  }
</style>
