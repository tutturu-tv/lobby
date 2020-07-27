<script>
  import PlayButton from "../assets/play-default.svg";
  export let sub
  export let a
  let experiment = a ? 'a' : 'b'
  let usertype = sub ? 'premium' : 'free'
</script>

<div>
  <div class="highlight-header-container">
    <h2 class="highlight-header">New Premium Feature!</h2>
    <h3 class="highlight-subheader">Save your favorite websites and extensions for next time!</h3>
  </div>
  {#if a}
  <div class="videoContainer">
    <div id="playBtn" class="play-btn">
      <PlayButton />
    </div>
    <div id="videoOverlay" />
    <video id="saveStateVid" class="vid" src="/ad.mp4" poster="tu-lobby-thumbnail.png" controls />
  </div>
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
  @keyframes slidebg {
    0%,
    100% {
      background-position: -450px;
    }
    50% {
      background-position: -0px;
    }
  }

  .comfy {
    margin-top: 2px;
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
    background-image: linear-gradient(45deg, #00C0FF 0%, #FFCF00 49%, #FC4F4F 80%, #00C0FF 100%);
    background-position: -250px;
    background-size: 800px 56px;
    animation: slidebg 4s ease-in-out infinite;
    cursor: pointer;
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

  .videoContainer {
    position: relative;
  }

  #videoOverlay {
    background: rgba(0,0,0,0.2);
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 12px;
  }

  .vid {
    width: 45rem;
    margin-bottom: 8px;
  }

  .vid:focus {
    outline: none !important;
  }

  .vid:hover {
    cursor: pointer;
  }

  .highlight-header-container {
    margin-bottom: 12px;
    margin-top: 12px;
  }

  .highlight-header {
    font-size: 24px;
    margin-bottom: 8px;
    margin-top: 0;
  }

  .highlight-subheader {
    font-size: 18px;
    font-weight: normal;
    margin: 4px auto;
  }

  .dim {
    color: #a1a7aa;
    font-size: 16px;
    line-height: 136%;
    margin-bottom: 10px;
  }

  .comfy:hover {
    background-color: #7a92f3;
  }

  .play-btn {
    position: absolute;
    left: calc(50% - 50px);
    top: calc(50% - 60px); 
    height: 100px;
    width: 100px;
    fill: white;
    opacity: 60%;
  }

  .play-btn:hover {
    opacity: 100%;
    cursor: pointer;
  }

</style>
