<template>
  <v-container>
    <div style="position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);">

      <v-card :loading="loading" class="mx-auto my-12" style="width:500px;">
        <h1 style="font-family: Verdana">Login</h1>

        <v-divider class="mx-4"></v-divider>

        <v-card-title>Username</v-card-title>

        <v-card-title>Password</v-card-title>

        <v-card-actions>
          <v-btn color="deep-purple lighten-2" text @click="reserve">
            Reserve
          </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "login",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
