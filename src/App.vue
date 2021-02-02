<template>
  <div
    v-on:click="moveDrone"
  class="drone-field">
    <h1>Drone test</h1>
    <drone-body :posTop="positionTop" :posLeft="positionLeft"></drone-body>
  </div>
</template>

<script>
import './App.scss';
import DroneBody from '@/components/DroneBody.vue';

export default {
  data() {
    return {
      positionTop: 200,
      positionLeft: 200,
    };
  },
  components: {
    DroneBody,
  },
  methods: {
    moveDrone(event) {
      const area = document.querySelector('.drone-field');
      const areaCoords = area.getBoundingClientRect();
      this.positionTop = event.clientY - areaCoords.top - area.clientTop - 60;
      this.positionLeft = event.clientX - areaCoords.left - area.clientLeft;
    },
  },
};
</script>
