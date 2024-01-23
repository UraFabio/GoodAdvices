<template>
  <div id="main-container">
    <NavBar />
    <div id="advices-container">
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
      <Advice />
    </div>
    <Footer />
  </div>
</template>

<script>
import Advice from "./components/Advice.vue"
import NavBar from "./components/NavBar.vue"
import Footer from "./components/Footer.vue"

export default {
  name: 'App',
  components: {
   Advice,
   NavBar,
   Footer
  },
};
</script>

<style>

*{
  margin: 0;
  padding: 0;
  border: 0;
}

#main-container {
  height: 100vh;
  min-width: 1024px;
  min-height: 768px;
}

#advices-container {
  padding-top: 20px;
  height: 100%;
  min-height: 538px;
  background-color: #ccc;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr; 
  grid-auto-rows: 250px;
  justify-items: center;
  align-items: center;
}

a{
  text-decoration: none;
  color: #ccc;
  margin: 12px;
  transition: .5s;
}

a:hover {
  color: #37a8f3;
}

</style>
