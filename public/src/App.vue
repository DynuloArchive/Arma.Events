<template>
  <div id="app">
    <Countdown />
    <section>
      <h2>Participating Units</h2>
      <div class="units">
        <UnitComponent v-for="unit in units" :key="unit.id" :unit="unit"/>
      </div>
    </section>
    <section>
      <h2>Apply</h2>
      <p>Currently Arma.Events is an invite only project.</p>
    </section>
    <section>
      <h2>About</h2>
      <p>Arma.Events is a community project by Dynulo to provide a group of communities with a consistent Joint OP experience. Each month a different community hosts an event using Dynulo's high performance cloud resources.</p>
    </section>
    <footer>
      &copy; Dynulo 2020
    </footer>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Countdown from "./components/Countdown.vue";
import UnitComponent from "./components/Unit.vue";
import Unit from "./unit";

@Component({
  components: {
    Countdown,
    UnitComponent,
  }
})
export default class App extends Vue {
  units: Unit[] = [{
    id: "apm",
    name: "Artamidae",
    image: require('@/assets/units/apm.png'),
  }, {
    id: "synixe",
    name: "Synixe",
    image: require('@/assets/units/synixe.png'),
  }, {
    id: "clover",
    name: "Clover",
    image: require('@/assets/units/clover.png'),
  }];
}
</script>

<style lang="scss">
body, html {
  height: 100%;
  margin: 0;
  background-color: #37474F;
  color: white;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  section {
    width: 80vw;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    padding-bottom: 3rem;
  }

  footer {
    width: 80vw;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    font-size: 0.8rem;
    padding-bottom: 2rem;
  }
}
</style>
