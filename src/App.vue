<template>
  <div id="app">
    <button v-on:click="title = 'title vua duoc thay doi tu component cha'">Click thay doi title</button>
    <HelloWorld v-bind:title="title"
    v-on:changTitleEvent = "handleChangeTitle"
    />
    <ListUser v-bind:listUser = "listUser"
    v-on:appDeleteUser = "appDeleteUser"
    />
    <CompFooter v-bind:title="title"/>
    <Ref />
    <demo-slot>
    <h3> day la du lieu kieu mot doan the html muon truyen vao component con</h3>
    </demo-slot>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ListUser from "./components/ListUser"
import CompFooter from "./components/CompFooter"
import Ref from "./components/Ref"
import demoSlot from "./components/demoSlot";
export default {
  name: 'App',
  data(){
    return{
      title: 'hello VueJs - header',
      listUser: [
        {id :100, email: ' email@gmail.com', active: true},
        {id :101, email: ' emailaer@gmail.com', active: false},
        {id :102, email: ' email23@gmail.com', active: true},
        {id :103, email: ' email23@gmail.com', active: true},
        {id :104, email: ' email2@gmail.com', active: false},
        {id :105, email: ' email4@gmail.com', active: true}
      ]
    }
  },
  components: {
    HelloWorld,
    ListUser,
    CompFooter,
    Ref,
    demoSlot,
  },
  methods: {
    handleChangeTitle(data){
      this.title = data.title;
    },
    appDeleteUser(data){
      var index = -1;
      this.listUser.forEach((u, idx) => {
        if (u.id === data.id){
          index = idx;
        }
      });
      if (index !== -1){
        this.listUser.splice(index, 1);
      }
      console.log('app da nhan duoc user', data);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
