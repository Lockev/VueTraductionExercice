<template>
  <div class="card">
    <div class="card-image">
      <img src="http://semantic-html.co.uk/images/pen2/cloud-mountain.jpg" />
    </div>
    <div class="card-text">
      <h2>{{ this.title }}</h2>
      <p>
        {{ this.description }}
      </p>
    </div>
    <div class="card-inner">
      <div>
        <button class="styled">Read More</button>
      </div>
      <div>
        <p><i class="fa fa-thumbs-o-up fa-lg" aria-hidden="true"></i></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: String,
    src: String,
    description: String
  },
  data() {
    return {
      // title: "test"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  box-sizing: border-box;
}

html {
  font-size: 14pt;
}

body {
  margin: 0;
  padding: 0;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  width: 100%;
  padding: 25px;
  background-color: black;
}

nav h2 {
  font-size: 1.5rem;
  margin: 0;
  padding: 0;
  color: white;
}

nav a {
  color: white;
}

.title {
  margin: 0;
  border: none;
}

.card {
  flex: 1 30%;
  display: flex;
  flex-direction: column;
  margin: 10px;
  background-color: #fff;
  border: 1px solid grey;
  border-radius: 5px;
  box-shadow: 0px 10px 15px 0 rgba(0, 0, 0, 0.3);
}
.card-image {
  margin: 0;
}
.card-image img {
  max-width: 100% !important;
  border-radius: 3px 3px 0 0;
}

.card-text {
  justify-self: flex-start;
  margin: 0;
  padding: 1rem;
}
.card-inner {
  display: flex;
  align-items: flex-end;
  margin: 0;
  padding: 1rem;
}
.card-inner div {
  flex: 0 1 50%;
}
.card-inner div p {
  margin: 0;
  padding: 0;
  text-align: right;
  color: blue;
}

button {
  background-color: #c20000;
  color: white;
}
button.styled {
  padding: 10px 20px;
  background: #c20000;
  border: none;
  border-radius: 5px;
  font-size: 0.85rem;
  color: white;
}
</style>
