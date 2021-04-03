<template>
<div class="app">
  <UserProfile/>
</div>
<!-- <div id='app'>
  @_{{user.userName}} - {{fullName}}
  <strong>Followers:</strong> {{user.followers}}
</div> -->
<!-- <button @click="followUser()">Follow</button> -->
</template>

<script>
import UserProfile from './components/Layout/UserProfile.vue';
export default {
  name: 'App',
  components: {
    UserProfile
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
