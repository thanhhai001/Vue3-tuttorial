<template>
  <div class="user-profile">
    <div class="user-profile-content">
      <h1>@_{{user.userName}}</h1>
      <div class="user-profile-role">
        {{user.roleName}}
      </div>
      <div class="user-profile-follower">
        Followers: {{user.followers}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'UserProfile',
    data() {
      return {
          user: {
            id : 1,
            userName: 'dark01',
            email: 'haicnt.iuh@gmail.com',
            firstName: 'Cao Ngoc Thanh',
            lastName: 'Hai',
            isAdmin: true,
            followers: 0,
            role: 1,
            roleName: 'Admin'
          }
      }
  },
  computed: {
    fullName() {
      return `${this.user.firstName} ${this.user.lastName}`;
    }
  },
  methods: {
    followUser() {
      this.user.followers++;
    }
  }
}
</script>

<style>
  .user-profile {
    display: grid;
    grid-template-columns: 1fr 3fr;
    width: 100%;
    padding: 50px 5%;
  }

  .user-profile-content {
    display: flex;
    flex-direction: column;
    margin-right: 50px;
    background: white;
    padding: 20px;
    border-radius: 5px;
    border: 1px solid #DFE3E8;
    text-align: left;
    
  }

  .user-profile-follower {

  }
</style>