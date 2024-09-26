<template>
  <div class="container">
    <button @click="startAnimation">Start Animation</button>
    <div v-if="showAnimation" :class="{ 'animated': showAnimation, 'bounce': showAnimation }">
      This element is animated!
    </div>
  </div>
</template>

<script>
import 'animate.css';
export default {
  data() {
    return {
      showAnimation: false
    }
  },
  methods: {
    startAnimation() {
      this.showAnimation = true;
      setTimeout(() => {
        this.showAnimation = false;
      }, 2000);
    }
  }
}
</script>