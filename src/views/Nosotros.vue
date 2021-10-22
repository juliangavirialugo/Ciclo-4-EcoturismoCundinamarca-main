<template>

  <div>
    <v-container>
      <v-row no-gutters justify="center" align="center">
        <h1 class=" font-weight-black mt-3">
          Nuestro <span class="font-weight-regular">Equipo</span>
        </h1>
      </v-row>
    </v-container>

    <div class="d-flex justify-center flex-wrap" tile>
      <v-card
        v-for="equipo in team"
        :key="equipo.name"
        class="mx-4 my-2"
        max-width="300"
      >
        <div class="d-flex justify-center mt-3">
          <v-avatar size="200">
            <img position="auto" :src="equipo.img" :alt="equipo.name" />
          </v-avatar>
        </div>

        <v-card-text>
          <h2 class="text-h5 red--text text-center ">{{ equipo.name }}</h2>
          <p class="text-h6 text-center">{{ equipo.text }}</p>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "team",
  components: {},
  data() {
    return {
      team: [
        {
          name: "Jimmy Rincón",
          img: require("../../src/assets/imgs/foto-jimmy.jpg"),
          text: "Ventas",
        },
        {
          name: "Sergio Ramos",
          img: require("../../src/assets/imgs/foto-sergio.jpg"),
          text: "Atención al cliente",
        },
        {
          name: "David Martinez",
          img: require("../../src/assets/imgs/foto-david.jpg"),
          text: "Supervisor de actividades",
        },
        {
          name: "Julian Gaviria",
          img: require("../../src/assets/imgs/foto-julian.jpg"),
          text: "Logística",
        },
        {
          name: "Sonia Pulido",
          img: require("../../src/assets/imgs/foto-sonia.jpg"),
          text: "Administración",
        },
              ],
    };
  },
};
</script>
