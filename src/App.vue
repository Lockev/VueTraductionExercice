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
      {{ sayHello || sayHelloEN }}
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "App",
  // components: {
  //   HelloWorld
  // }
  data() {
    return {
      sayHelloFR: "Bonjour",
      sayHelloES: "Holà",
      sayHelloEN: "Hello",
      // currentLanguage: "en",
      sayHello: "Hello"
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
</style>
