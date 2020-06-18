<template>
  <v-layout column justify-center align-center>
    <v-container>
      <v-row>
        <v-col v-for="(personaje, index) in personajes" :key="index" cols="4">
          <v-card>
            <v-img class="white--text align-end" :src="personaje.imagen">
            </v-img>
            <v-card-title class="headline">
              {{ personaje.nombre }}
            </v-card-title>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
export default {
  components: {},
  computed: {
    personajes() {
      return this.$store.state.personajes.personajes;
    }
  }
};
</script>
