<template>
  <div id="app">
    <Welcome :isLoading="isLoading" />
    <main v-if="!isLoading">
      <router-view/>
    </main>
  </div>
</template>
<script>
import Welcome from '@/components/Welcome'
export default {
  name: "App",
  components: {
    Welcome
  },
  data() {
    return { isLoading: true };
  },
  mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 3500);
  }
};
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

:root {
  --primaryColor: #FF5722;
  --secondaryColor: #FFCCBC;
  --accentColor: #2e302f;
  --errorColor: #fe2a39;
}

#app {
  font-family: 'Poppins', sans-serif;;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
  background-color: var(--accentColor);
}

h1 {
  text-align: center;
}
</style>
