<template>
  <v-toolbar fixed class="cyan" dark fluid>
    <v-toolbar-title class="mr-4">
      <span
      class = "home"
        @click="navigateTO({name: 'root'})">
      TabTracker
    </span>
    </v-toolbar-title>

    <!-- TODO: Implement ME -->
    <!-- <v-toolbar-items>
      <v-btn flat dark>Browse</v-btn>
    </v-toolbar-items> -->
      <v-spacer></v-spacer>

      <v-toolbar-items>
              <v-btn
                  v-if = "!$store.state.isUserLoggedIn"
                  flat dark
                  @click="navigateTO({name: 'register'})">
                  Sign Up
                </v-btn>
              <v-btn
                  v-if = "!$store.state.isUserLoggedIn"
                  flat dark
                  @click="navigateTO({name: 'login'})">
              Login</v-btn>
      </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  methods: {
    navigateTO (route) {
      this.$router.push(route)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home {
  cursor: pointer;
}
.home:hover {
  color: #E9E;
}
</style>
