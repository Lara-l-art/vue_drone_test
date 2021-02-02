<template>
  <div
    :style="{ top: posTop + 'px', left: posLeft + 'px' }"
    class="drone"
  >
    <div class="drone__body">
      <div class="drone__body-left"></div>
      <div class="drone__body-right"></div>
      <div class="drone__body-triangle-top"></div>
      <div class="drone__body-triangle-bottom"></div>
    </div>
    <wings></wings>
  </div>
</template>

<script>
import Wings from '@/components/Wings.vue';
import './DroneBody.scss';

export default {
  name: 'HelloWorld',
  components: { Wings },
  props: {
    posTop: Number,
    posLeft: Number,
  },
};
</script>
