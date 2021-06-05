<template>
  <v-container>
    <div
      style="
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      "
    >
      <v-card :loading="loading" class="mx-auto my-12" style="width:500px;">
        <v-tabs
          v-model="tab"
          background-color="indigo lighten-1"
          centered
          dark
          icons-and-text
        >
          <v-tabs-slider></v-tabs-slider>

          <v-tab style="font-family: Verdana" href="#tab-1">
            Login
            <v-icon>mdi-login</v-icon>
          </v-tab>

          <v-tab style="font-family: Verdana" href="#tab-2">
            Register
            <v-icon>mdi-account-plus</v-icon>
          </v-tab>
        </v-tabs>

        <v-tabs-items v-model="tab">
          <v-tab-item v-for="i in 3" :key="i" :value="'tab-' + i">
            <v-card flat>
              <v-card-text>{{ text }}</v-card-text>
            </v-card>
          </v-tab-item>
        </v-tabs-items>
        <center>
        <v-card-title style="text-align:center !important;">Username</v-card-title>
        <v-text-field style="width:400px;"></v-text-field>
        <v-card-title>Password</v-card-title>
        <v-text-field style="width:400px;"></v-text-field>
        </center>
        <v-card-actions>
          <v-row justify="end">
            <v-btn
              class="mx-5"
              fab
              dark
              color="indigo lighten-1"
              @click="submit">
              <v-icon>mdi-chevron-right</v-icon>
            </v-btn>
          </v-row>
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
