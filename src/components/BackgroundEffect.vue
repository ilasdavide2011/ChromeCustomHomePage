<template>
  <div 
    id="blob"
    :style="{left: mx + 'px', top: my + 'px'}" 
    ></div>
  <div id="blur"></div>
</template>

<script>
  export default {
    data() {
      return {
        mx: 100,
        my: 100,
      }
    },
    mounted() {
      document.addEventListener("mousemove", (event) => {
        this.mx = event.clientX-250;
        this.my = event.clientY-250;
      });
    }
  }
</script>

<style scoped>
#blob {
  background: #fff;
  height: 500px;
  aspect-ratio: 1;
  position: absolute;
  border-radius: 50%;
  background: linear-gradient(to top, #9795f0 0%, #fbc8d4 100%);
  animation: rotate 10s infinite;
}
#blur {
  height: 100%;
  width: 100%;
  position: absolute;
  z-index: 2;
  backdrop-filter: blur(200px);
  margin: 0px;
  left: 0;
  top: 0;
}

@keyframes rotate {
  from {
    rotate: 0deg;
  }
  50% {
    scale: 1 1.15;
  }
  to {
    rotate: 360deg;
  }
}
</style>
