<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div id="nav">
      <div class='inline-block' @click='goHome'>Home</div> |
      <div class='inline-block' @click='goAbout'>About</div> |
      <div class='inline-block' @click='goUser'>User</div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  methods:{
      goHome(){
          console.log('goHome');
      },
      goAbout(){
          console.log('goAbout');
          this.$router.push({
              name:'About',
              params: {
                  info:'Hello',
              }
          })
      },
      goUser(){
          console.log('goUser');
          this.$router.push({
              name: 'User',
              params:{
                  id: 1
              }
          })
      }

  }
}
</script>

<style scoped>
.inline-block{
    display: inline-block;
}
</style>
