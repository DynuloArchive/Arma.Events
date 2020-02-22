<template>
  <div class="unit">
    <img :src="unit.image" />
    <span class="name">{{ unit.name }}</span>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import Unit from '../unit';

@Component
export default class UnitComponent extends Vue {
  @Prop() private unit!: Unit;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.unit {
  display: inline-block;
  padding-left: 1.5rem;
  padding-right: 1.5rem;
  width: 12rem;
}
img {
  width: 150px;
  height: 150px;
}
.name {
  display: block;
  font-size: 1.7rem;
}
</style>
