<template>
  <v-btn class="login-button" color="warning" depressed large @click="logout"
    >Logout</v-btn
  >
</template>

<script>
export default {
  logout() {
    const that = this
    this.$fire
      .auth()
      .signOut()
      .then((user) => {
        that.$router.push('/')
      })
  },
}
</script>
