<template>
  <v-app>
    <v-container class="my_container fill-height justify-center" fluid>
      <v-row class="block justify-center">
        <!-- <v-col md="6" lg="4" sm="12" xs="12" cols="12">
          <h1 :class="height >= 500 ? 'my_title' : 'my_title_mobile'">
            apropos
          </h1>
        </v-col>
        <v-col
          :class="height >= 500 ? 'right_col' : 'right_col_mobile'"
          md="6"
          lg="4"
          sm="12"
          xs="12"
          cols="12"
        > -->
        <img src="./assets/apropos_logo.png" class="logo_app" />
        <!-- </v-col> -->
      </v-row>
    </v-container>
    <v-footer padless color="#FFFFFF">
      <v-col class="text-right" cols="12">
        <span style="color: black" class="my_footer"> Apropos © 2022. </span>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
  computed: {
    height() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return 220;
        case "sm":
          return 400;
        case "md":
          return 500;
        case "lg":
          return 600;
        case "xl":
          return 800;
      }
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
.my_container {
  background-color: #ffffff;
}

.my_title {
  color: black;
  font-size: 80px;
  font-family: "Poppins", sans-serif;
  animation-name: FadeIn;
  animation-duration: 6s;
  transition-timing-function: ease-in-out;
  text-align: end;
}

.my_title_mobile {
  color: #eceff1;
  font-size: 80px;
  font-family: "Poppins", sans-serif;
  animation-name: FadeIn;
  animation-duration: 6s;
  transition-timing-function: ease-in-out;
  text-align: center;
}

.right_col {
  border-left: 1px solid grey;
  animation-name: FadeIn;
  animation-duration: 8s;
  transition-timing-function: ease-in-out;
}

.logo_app {
  animation: rotation 20s linear infinite;
    height: auto;
    max-width: 300px;;
}

@keyframes rotation {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}

.my_icon {
  margin-left: 30px;
  cursor: pointer;
}

.text_coming {
  color: #64b5f6;
  font-family: "Poppins", sans-serif;
  font-weight: bold;
  font-style: italic;
}

.text_connect {
  color: black;
  font-family: "Poppins", sans-serif;
}

.text_coming_mobile {
  color: black;
  font-family: "Poppins", sans-serif;
  font-weight: bold;
  font-style: italic;
  text-align: center;
}

.text_connect_mobile {
  color: black;
  font-family: "Poppins", sans-serif;
  text-align: center;
}

.my_footer {
  color: black;
  font-family: "Poppins", sans-serif;
  font-size: 11px;
}
</style>