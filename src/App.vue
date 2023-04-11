<template>
  <nav class="nav">
    <i class="fa-solid fa-xmark" @click="hideMenu"></i>
    <ul class="lists">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/tech">Technology</router-link>
    </ul>
  </nav>
  <i class="fa-solid fa-bars" @click="showNavbar" v-if="hideMenuIcon"></i>
  <router-view/>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      hideMenuIcon: true,
    }
  },
  methods: {
    showNavbar() {
     const nav = document.querySelector(".nav")
     nav.classList.toggle('transform')
     this.hideMenuIcon = !this.hideMenuIcon
    },
    hideMenu() {
     this.hideMenuIcon = !this.hideMenuIcon
     const nav = document.querySelector(".nav")
     nav.classList.toggle('transform')
    }
  }
}
</script>

<style>
.transform {
  transform: translateX(0);
}
.transform-against {
  transform: translateX(305px);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  overflow-x: hidden;
}
nav {
  padding: 30px;
  position: absolute;
  background-color: #666;
  width: 20%;
  height: 100vh;
  right: 0;
  transform: translateX(305px);
  transition: 0.5s all ease;
}

.lists {
  display: flex;
  flex-direction: column;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  display: inline-block;
  margin-top: 20px;
}
.fa-bars {
  position: absolute;
  right: 20px;
  top: 20px;
  font-size: 24px;
  cursor: pointer;
}
.fa-xmark {
  position: absolute;
  left: 30px;
  font-size: 24px;
  cursor: pointer;
}
</style>
