<div class="container">
  <img class="discord-icon" alt="Join our Discord server!" src="discord.png" width="150" />
  <p class="name">Tutturu!</p>
  <div class="line"></div>
  <p class="members" id="members">??? members</p><button id="join-discord" class="join">Join server</button>
</div>

<style>
  .container {
    background-color: #2e2e2e;
    box-sizing: border-box;
    width: 270px;
    position: absolute;
    right: 0;
    top: 58px;
    text-align: left;
    color: #a1a7aa;
    font-weight: 600;
    padding: 8px 16px 12px 16px;
  }
  .discord-icon {
    margin-left: -8px;
  }
  .name {
    font-weight: bold;
    font-size: 13px;
    margin-bottom: 6px;
    margin-top: 0;
  }
  .line {
    background-color: #a1a7aa;
    height: 1px;
    width: 96%;
    margin-bottom: 8px;
  }
  .members {
    margin-right: 12px;
    font-weight: normal;
    display: inline;
    text-transform: uppercase;
  }
  .join {
    display: inline;
    text-transform: uppercase;
    margin-bottom: 0;
    margin-left: 0.625rem;
    margin-top: 2px;
    background-color: #627ff1;
    text-shadow: 0 0 1px #eee;
    width: fit-content;
    border-radius: 7.5rem;
    font-size: 9pt;
    padding: 0.9375rem 1.25rem;
    display: inline-block;
    color: white;
    border: 0;
  }
  .join:hover {
    background-color: #7a92f3;
    cursor: pointer;
  }
</style>
