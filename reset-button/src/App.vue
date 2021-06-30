<template>
  <div id="app"> 
    <button @click="showConfetti" class="reset-btn">RESET</button>
  </div>
</template>

<script>
import JSConfetti from 'js-confetti'

export default {
  data() {
    return {
      jsConfetti: null
    }
  },
  methods: {
    showConfetti() {
      this.jsConfetti.addConfetti({
        confettiRadius: 10, confettiNumber: 200
      });
    }
  },
  mounted() {
    this.jsConfetti = new JSConfetti();
  }
}
</script>

<style>
body {
  
  background-color: rgb(51, 50, 50);
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.reset-btn {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  background-color: #4f67d3;
  color: white;
  font-weight: 600;
  margin: auto;
  font-size: 40px;
  margin: auto;
  text-shadow: 0px 8px #3f3636;
  outline:none;
}

.reset-btn:active {
  background-color: #35489b;
  padding-top: 8px;
  text-shadow: 0px 6px #3f3636;
}
</style>
