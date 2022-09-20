<template>
  <div class="api">
    <br />
    <h2>Appeler une API</h2>
    <br />
    <button class="button button2" @click="creationItem">data</button>
    <p>
      {{ list.data }}
    </p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "api-stor",
  data() {
    return {
      list: {},
    };
  },
  computed: {},
  methods: {
    async creationItem() {
      this.list = await axios.get("https://random-data-api.com/api/v2/banks");
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
.button2 {
  background-color: #008cba; /* Blue */
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
</style>
