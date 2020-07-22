<div class="container">
  <img alt="Join our Discord server!" src="discord.png" width="150" />
  <p class="name">Tutturu!</p>
  <div class="line"></div>
  <p class="members">??? members</p><button id="join-discord" class="join">Join server</button>
</div>

<style>
  .container {
    background-color: #2e2e2e;
    width: 20rem;
    position: absolute;
    right: 0;
    top: 3.125rem;
    text-align: left;
    color: #a1a7aa;
    font-weight: 600;
    padding: 0.625rem 0.625rem 1.00rem;
  }
  .name {
    margin-top: 0.1875rem;
    margin-bottom: 0.3125rem;
  }
  .line {
    background-color: #a1a7aa;
    height: 1px;
    width: 16.875rem;
    margin-bottom: 1.25rem;
  }
  .members {
    display: inline;
    text-transform: uppercase;
  }
  .join {
    display: inline;
    text-transform: uppercase;

    background-color: #627ff1;
    text-shadow: 0 0 1px #eee;
    width: fit-content;
    border-radius: 7.5rem;
    font-size: 9pt;
    padding: 0.9375rem 1.25rem;
    display: inline-block;
    color: white;
    margin-left: 0.625rem;
    border: 0;
  }
  .join:hover {
    background-color: #7a92f3;
  }
</style>
