<template>
  <div id="app">
    <div>Toki Pona is a language that in itself literally means "(language|to speak|spoken) (simple|good)"</br>
    It has only the numbers, 1 (wan), 2 (tu), 5 (luka), 100 (mute). The words are always lowercase unless it is a non Toki Pona word, in which case it is uppercase.</br>

    Please enter your phone number below in the format "My number is 451 million 234 thousand 567" but in Toki Pona of course.</br>
    </div>
    <hello></hello>
    <span> Hint: "mi jo nunpa e" means "My phone number is" </span>
  </div>
</template>

<script>
import Hello from './components/Hello'

export default {
  name: 'app',
  components: {
    Hello
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
