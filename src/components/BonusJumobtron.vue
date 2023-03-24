<script>
export default {
  data(){
      return {
        imgLink: `https://picsum.photos/${window.screen.width}/${Math.floor(window.screen.height/2)}`,
      }
    },
  methods : {
    getJumbotronLink(){
      return new URL (this.imgLink, import.meta.url).href;
    }
  }
}
  
</script>

<template>
  <div class="jumbotron" :style="`background-image:url(${getJumbotronLink()})`">
  </div>
</template>

<style scoped>
.jumbotron {
  background-size: cover;
  background-position: center;
  width: 100%;
  height: calc(100vh / 2);
}
</style>