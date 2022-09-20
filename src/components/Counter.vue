<template>
  <div class="Counter">
    <h2>Counter: {{ counter }}</h2>
    <button class="button" @click="increase">+</button>
    <button class="button button3" @click="decrease">-</button>
  </div>
</template>

<script>
export default {
  name: "Counter-stor",
  computed: {
    counter() {
      return this.$store.state.counter;
    },
  },
  methods: {
    increase() {
      this.$store.state.counter++;
    },
    decrease() {
      this.$store.state.counter--;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
.button {
  background-color: #4caf50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}
.button3 {
  background-color: #f44336;
} /* Red */
</style>
