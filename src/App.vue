<template>
  <div id="app">
    <div class="flags">
      <!-- <img alt="Drapeau France" src="./assets/flag-FR.jpg" v-on:click="changeLanguage('fr')" />
      <img alt="Drapeau Espagne" src="./assets/flag-ES.png" v-on:click="changeLanguage('es')" />
      <img alt="Drapeau UK" src="./assets/flag-UK.jpg" v-on:click="changeLanguage('en')" />
      {{ sayHello || sayHelloEN }} -->
      <img alt="Drapeau France" src="./assets/flag-FR.jpg" v-on:click="sayHello = sayHelloFR" />
      <img alt="Drapeau Espagne" src="./assets/flag-ES.png" v-on:click="sayHello = sayHelloES" />
      <img alt="Drapeau UK" src="./assets/flag-UK.jpg" v-on:click="sayHello = sayHelloEN" />
    </div>
    {{ sayHello || sayHelloEN }}
    <!-- {{ cardsData }} -->
    <div class="card-wrapper">
      <Card v-for="card in cardsData" :key="card" :title="card.title" :src="card.src" :description="card.description"></Card>
    </div>
  </div>
</template>

<script>
import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    Card
  },
  data() {
    return {
      // currentLanguage: "en",
      sayHelloFR: "Bonjour",
      sayHelloES: "Holà",
      sayHelloEN: "Hello",
      sayHello: "Hello",
      cardsData: [
        {
          title: "Titre 1",
          src: "https://media.gettyimages.com/photos/young-rabbit-on-hand-picture-id106145687",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
        },
        {
          title: "Titre 2",
          src: "https://media.gettyimages.com/photos/young-rabbit-on-hand-picture-id106145687",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
        },
        {
          title: "Titre 3",
          src: "https://media.gettyimages.com/photos/young-rabbit-on-hand-picture-id106145687",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
        }
      ]
    };
  }
  // method: {
  //   changeLanguage: function(lang) {
  //     this.currentLanguage = lang;
  //   }
  // },
  // computed: {
  //   sayHello: function() {
  //     let displayHello = "";
  //     switch (this.currentLanguage) {
  //       case "fr":
  //         displayHello = this.sayHelloFR;
  //         break;
  //       case "es":
  //         displayHello = this.sayHelloES;
  //         break;
  //       case "en":
  //         displayHello = this.sayHelloEN;
  //     }
  //     return displayHello;
  //   }
  // }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.flags {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
img {
  width: 150px;
}

.card-wrapper {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}
</style>
