<template>
  <div class="hello">
    <input v-on:input="translate" v-model="message" placeholder="What is your phone number?"></input>
    <p> Your phone number is: {{ number }} </p>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      number: 'invalid',
      message: ''
    }
  },
  methods: {
    translate: function () {
      if (this.message.indexOf('mi jo nunpa e') === 0) {
        var count = 0
        var message = this.message.split('mi jo nunpa e')[1].split(' ')
        for (var i = 0; i < message.length; i++) {
          if (message[i] === 'mute') {
            count += 100
          } else if (message[i] === 'luka') {
            count += 5
          } else if (message[i] === 'tu') {
            count += 2
          } else if (message[i] === 'wun') {
            count += 1
          }
        }
        this.number = count
      } else {
        this.number = 'invalid'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
