<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title class="headline"> Login to the account </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="Username"></v-text-field>
            <v-text-field label="Password"></v-text-field>
          </v-form>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/login"> Login </v-btn>
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
