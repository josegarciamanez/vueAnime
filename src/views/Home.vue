<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h2>Jose García Máñez</h2>
    <HelloWorld msg="Vue.js & Anime.js"/>
    <button @click="animacion">Anime</button>
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld.vue";
import anime from '../../node_modules/animejs'

export default {
  name: "home",
  components: {
    HelloWorld
  },
  methods: {
    animacion() {
        anime({
            targets: "h2",
            translateY: [
                { value: 250, duration: 1500 },
                { value: 0, duration: 1500 }
            ],
            translateX: [
                { value: 50, duration: 1500 },
                { value: 0, duration: 1500 }
            ],
            rotate: "1turn",
            // backgroundColor: "#000",
            duration: 3000,
            loop: false
        });
    }
  }
};
</script>
