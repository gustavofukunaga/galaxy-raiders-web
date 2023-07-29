<template>
  <div id="canvas">
    <div id="deep-space" />
    <div id="menu">
      <h1>GALAXY RAIDERS</h1>
      <button><router-link class="menu-button" to="/game">Start</router-link></button>
      <button><router-link class="menu-button" to="/leaderboard">Leaderboard</router-link></button>
      <button class="menu-button" onclick="window.location.href='https://google.com';">Exit</button>
    </div>
  </div>
</template>

<style>

#canvas {
  height: calc(100vh - 4rem);
  width: calc(100vw - 4rem);

  padding: 2rem;

  background-color: #36bbf5;
  overflow: hidden;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}

#deep-space {
  height: calc(100% - 4rem);
  width: calc(100% - 4rem);

  background-image: url("~/assets/space.png");
  background-origin: content-box;
  animation: slide 3s linear infinite;

  position: absolute;
  z-index: 0;
}

#menu {
  height: calc(100% - 4rem);
  width: calc(100% - 4rem);
  
  color: yellow;
  font-size: large;

  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.menu-button {
  background-color: grey;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
</style>
