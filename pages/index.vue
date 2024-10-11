<template>
  <v-app>
    <v-container fluid class="d-flex flex-column justify-center align-center ">
      <h1 class="title">Bienvenue sur la page principale</h1>
      
      <!-- Section contenant les blocks -->
      <v-row class="block-container">
        <v-col
          v-for="(block, index) in blocks"
          :key="index"
          cols="auto"
          class="block"
          @click="navigateTo(block.link)"
        >
          <v-card class="block-card">
            <v-card-text class="d-flex flex-column align-center justify-center ">
              <v-img :src="block.icon" width="60" height="72"></v-img>
              <figcaption>{{ block.caption }}</figcaption>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      blocks: [
        {
          icon: '/icons/arrival.svg', // Remplacez par le bon chemin vers l'icône SVG
          caption: 'Infos arrivée',
          link: '/infos-arrivee'
        },
         {
          icon: '/icons/arrival.svg', // Remplacez par le bon chemin vers l'icône SVG
          caption: 'Infos arrivée',
          link: '/infos-arrivee'
        },
         {
          icon: '/icons/arrival.svg', // Remplacez par le bon chemin vers l'icône SVG
          caption: 'Infos arrivée',
          link: '/infos-arrivee'
        },
         {
          icon: '/icons/arrival.svg', // Remplacez par le bon chemin vers l'icône SVG
          caption: 'Infos arrivée',
          link: '/infos-arrivee'
        },
         {
          icon: '/icons/arrival.svg', // Remplacez par le bon chemin vers l'icône SVG
          caption: 'Infos arrivée',
          link: '/infos-arrivee'
        },
        // Ajoutez d'autres blocks ici
      ]
    }
  },
  methods: {
    navigateTo(link) {
      this.$router.push(link);
    }
  }
}
</script>

<style scoped>
.title {
  font-size: 25px;
  text-align: center;
  margin-bottom: 20px;
}

.block-container {
  justify-content: center;
  text-align: center;
}

.block {
  margin: 22px;
}

.block-card {
  width: 161px;
  height: 161px;
  border-radius: 15px;
  cursor: pointer;
  transition: transform 0.3s ease-in-out;
}

.block-card:hover {
  transform: scale(1.05);
}

figcaption {
  margin-top: 10px;
  font-size: 16px;
}
</style>
