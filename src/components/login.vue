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
      <v-card :loading="loading" class="mx-auto my-12" style="width: 500px">
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

        <center>
          <v-card-title>Username</v-card-title>
          <v-text-field v-model="userName" style="width: 400px"></v-text-field>
          <v-card-title>Password</v-card-title>
          <v-text-field v-model="password" type="password" style="width: 400px"></v-text-field>
        </center>

        <v-row justify="end">
          <v-btn
            class="mx-5"
            fab
            dark
            color="indigo lighten-1"
            @click="submit()"
          >
            <v-icon>mdi-chevron-right</v-icon>
          </v-btn>
        </v-row>
      </v-card>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "login",

  data: () => ({
    userName: "",
    password: "",
  }),

  methods: {
    submit() {
      if ((this.userName === "p") && (this.password === "s")) {
        console.log("success");
      } else {
        console.log("errosdr");
      }
    },
  },
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
.v-text-field {
  font-size: 30px !important;
}
</style>
