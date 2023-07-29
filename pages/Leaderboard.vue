<template>
  <div id="canvas">
    <div id="deep-space" />
    <div id="leaderboard">
      <h1>Leaderboard</h1>
      <table id="leaderboard-data">
        <thead>
          <tr>
            <th>Start time</th>
            <th>Destroyed asteroids</th>
            <th>Score</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="data in leaderboard" :key="data.dateTime">
            <td>{{ data.startTime }}</td>
            <td>{{ data.destroyedAsteroids }}</td>
            <td>{{ data.Score }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import JSON from '~/Leaderboard.json'

export default{
  data(){ return{ leaderboard: JSON } }
}
</script>

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

#leaderboard {
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

#game-title {
  color: #36bbf5;
}
</style>
