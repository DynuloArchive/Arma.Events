<template>
  <div class="bg">
    <div class="layer">
      <div class="countdown">
        <h1>Arma.Events</h1>
        <h2>Arma 3 Joint OP Community</h2>
        <h3 style="display: none">Out Next Event Starts in</h3>
        <h4>No Planned Events</h4>
        <div class="column">
          <h4 class="data">{{ days }}</h4>
          Days
        </div>
        <div class="column">
          <h4 class="data">{{ hours }}</h4>
          Hours
        </div>
        <div class="column">
          <h4 class="data">{{ minutes }}</h4>
          Minutes
        </div>
        <div class="column">
          <h4 class="data">{{ seconds }}</h4>
          Seconds
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Countdown extends Vue {
  days = 1;
  hours = 4;
  minutes = 32;
  seconds = 14;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/background.scss";
.bg {
  /* The image used */
  @include background-image;
  height: 100vh;

  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;

  .layer {
    background-color: rgba(0, 0, 0, 0.4);
    width: 100%;
    height: 100%;
    .countdown {
      width: 50vw;
      margin-left: auto;
      margin-right: auto;
      padding-top: 10rem;
      text-align: center;
      color: white;
      .column {
        background-color: rgba(0, 0, 0, 0.5);
        display: inline-block;
        width: 4rem;
        font-size: 0.7rem;
        padding: 2rem;
        display: none;
        h4 {
          font-size: 1.5rem;
          padding: 0;
          line-height: 0;
        }
      }
    }
  }
}
</style>
