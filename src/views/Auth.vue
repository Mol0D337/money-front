<template>
  <div class="wrapper-auth">
    <vue-telegram-login
            radius="10"
            userpic="false"
            requestAccess="write"
            mode="callback"
            telegram-login="manager_money_bot"
            @callback="getUserInfo"
    />
  </div>
</template>

<script>
  import {vueTelegramLogin} from 'vue-telegram-login'
  export default {
    name: "Auth",
    components: {vueTelegramLogin},
    methods: {
      getUserInfo (user) {
        console.log(user)
      }
    }
  }
</script>

<style scoped lang="sass">
.wrapper-auth
  height: 100vh
  display: flex
  justify-content: center
  align-items: center
</style>
