<template>
  <div class="hello">
    <h1>{{ title }}
      <br>
      <button v-on:click="changTitleHeader">Thay doi title tu compHeader.vue</button>
    </h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String
  },
  data(){
    return {
    }
  },
  methods: {
    changTitleHeader() {
      var data = {
        title: "test -> data truyen thong qua bien event"
      };
      console.log("truoc khi kich hoat su kien");

      this.$emit('changTitleEvent', data);
      console.log('sau khi kich hoat su kien');

      console.log(this);
    }
  }
}
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
</style>
