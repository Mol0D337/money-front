<template>
  <div class="wrapper-auth">
    <vue-telegram-login
            mode="callback"
            telegram-login="manager_money_bot"
            @callback="yourCallbackFunction"
    />
  </div>
</template>

<script>
  import {vueTelegramLogin} from 'vue-telegram-login'
  export default {
    name: "Auth",
    components: {vueTelegramLogin},
    methods: {
      yourCallbackFunction (user) {
        // gets user as an input
        // id, first_name, last_name, username,
        // photo_url, auth_date and hash
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
