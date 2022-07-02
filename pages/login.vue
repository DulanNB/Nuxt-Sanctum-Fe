<template>
  <a href="#" @click.prevent="login">Login</a>
</template>

<script>
export default {
  layout : 'default',
  methods:{
    login(){
      try {
        this.$auth.loginWith('laravelSanctum', {
          data: {
              email:'dulan418@gmail.com',
              password:'password'
          }
        })
      }catch (error) {
        console.log(error)
      }
    }
  }
}
</script>
