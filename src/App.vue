<script setup>
import { ref, watch } from "vue";

const slider = ref(2.89);
const background = ref('');

watch(slider, (oldValue, newValue) => {

})
</script>

<template>
  <div class="container-global">
    <div class="container-capa">
      <img class="capa" src="./assets/capa-folklore.jpg" alt="">
    </div>
    <div class="container-info">
      <div class="container-nome">
        <h2 class="nome-musica">august</h2>
        <p class="nome-cantora">Taylor Swift</p>
      </div>
      <div class="container-player">
        <div class="container-slider">
          <input type="range" class="slider" min="0.00" max="4.22" step="0.01" v-model="slider" name="" id="">
        </div>
        <div class="container-tempo">
          <div class="tempo-atual">2:42</div>
          <div class="tempo-total">4:22</div>
        </div>
        <div class="container-reproducao">
          <div class="container-aleatorio">
            <!-- <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-shuffle" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M0 3.5A.5.5 0 0 1 .5 3H1c2.202 0 3.827 1.24 4.874 2.418.49.552.865 1.102 1.126 1.532.26-.43.636-.98 1.126-1.532C9.173 4.24 10.798 3 13 3v1c-1.798 0-3.173 1.01-4.126 2.082A9.6 9.6 0 0 0 7.556 8a9.6 9.6 0 0 0 1.317 1.918C9.828 10.99 11.204 12 13 12v1c-2.202 0-3.827-1.24-4.874-2.418A10.6 10.6 0 0 1 7 9.05c-.26.43-.636.98-1.126 1.532C4.827 11.76 3.202 13 1 13H.5a.5.5 0 0 1 0-1H1c1.798 0 3.173-1.01 4.126-2.082A9.6 9.6 0 0 0 6.444 8a9.6 9.6 0 0 0-1.317-1.918C4.172 5.01 2.796 4 1 4H.5a.5.5 0 0 1-.5-.5"/>
              <path d="M13 5.466V1.534a.25.25 0 0 1 .41-.192l2.36 1.966c.12.1.12.284 0 .384l-2.36 1.966a.25.25 0 0 1-.41-.192m0 9v-3.932a.25.25 0 0 1 .41-.192l2.36 1.966c.12.1.12.284 0 .384l-2.36 1.966a.25.25 0 0 1-.41-.192"/>
            </svg> -->
            <img src="./assets/reproducao-aleatoria.png" alt="">
          </div>
          <div class="container-controler">
            <div class="prev">
              <img src="./assets/prev.png" alt="">
            </div>
            <div class="container-play">
              <div class="button-play">
                <img class="play" src="./assets/play.png" alt="">
              </div>
            </div>
            <div class="next">
              <img src="./assets/next.png" alt="">
            </div>
          </div>
          <div class="container-repetir">
            <img src="./assets/repetir-musica.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.container-global {
  display: flex;
  flex-direction: column;
  background-color: #3d3d3d;
  width: 100%;
  height: 100vh;
  gap: 20px;
}

.container-capa {
  height: 495px;
  display: flex;
  justify-content: center;
  align-items: flex-end;
}

.capa {
  position: relative;
  top: 55px;
  width: 80%;
  width: 440px;
  height: 440px;
  border-radius: 10px;
}

.container-info {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  width: 100%;
  height: 421px;
}

.container-nome {
  width: 440px;
}

.nome-musica  {
  color: #FDFDFD;
  font-weight: bold;
  letter-spacing: 0.5px;
  font-family: 'Roboto', sans-serif;
}

.nome-cantora {
  color: #a2a2a2;
  font-weight: 400;
  font-family: 'Roboto', sans-serif;
}

.container-player {
  width: 440px;
  margin-top: 50px;
}

.slider {
  -webkit-appearance: none;
  appearance: none;
  width: 100%;
  height: 2px;
  background: linear-gradient(to right, white 68%, white 0%, gray 0%, gray 100%);
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 14px;
  height: 14px;
  background-color: #FDFDFD;
  color: #FDFDFD;
  border-radius: 50%;
}

.container-tempo {
  width: 440px;
  display: flex;
  justify-content: space-between;
}

.tempo-atual, .tempo-total {
  font-family: 'Roboto', sans-serif;
  font-size: 14px;
  color: #bdbdbd;
  margin-top: 5px;
}

.container-reproducao {
  width: 440px;
  display: flex;
  justify-content: space-between;
  margin-top: 20px;
}

.container-aleatorio {
  color: #FDFDFD;
}

.container-controler {
  position: relative;
  left: 6px;
  bottom: 25px;
  display: flex;
  align-items: center;
  column-gap: 30px;
}

.button-play {
  width: 80px;
  height: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  background-color: #FDFDFD;
}

.play {
  position: relative;
  left: 1px;
}
</style>
