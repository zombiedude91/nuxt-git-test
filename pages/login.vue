<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title class="headline"> Login to the account </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field
              v-model="auth.email"
              label="Login"
              name="login"
              prepend-icon="mdi-account"
              type="text"
            ></v-text-field>
            <v-text-field
              v-model="auth.password"
              label="Password"
              name="password"
              prepend-icon="mdi-lock"
              type="password"
            ></v-text-field>
          </v-form>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            class="login-button"
            color="primary"
            depressed
            large
            @click="login"
            >Login</v-btn
          >
        </v-card-actions>
      </v-card>
      <div class="signup">
        <br />
        <p>
          Don't have account?
          <a href="/inspire" target="_blank" rel="noopener noreferrer">
            Sign Up </a
          >here.
        </p>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      snackbar: false,
      snackbarText: 'No error message',
      auth: {
        email: '',
        password: '',
      },
    }
  },
  methods: {
    login() {
      const that = this
      this.$fire.auth
        .signInWithEmailAndPassword(this.auth.email, this.auth.password)

        .catch(function (error) {
          that.snackbarText = error.message
          that.snackbar = true
        })
        .then((user) => {
          // we are signed in
          that.$router.push('/shop')
        })
    },
    forgotPassword() {
      const that = this
      this.$fire.auth
        .sendPasswordResetEmail(this.auth.email)

        .then(function () {
          that.snackbarText = 'reset link sent to ' + that.auth.email
          that.snackbar = true
        })
        .catch(function (error) {
          that.snackbarText = error.message
          that.snackbar = true
        })
    },
  },
}
</script>
