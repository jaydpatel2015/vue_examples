<template>
  <img src="./assets/logo.png" alt="vue">
  <Home data="This is home component" />
</template>

<script>
import Home from './components/Home.vue';

export default {
    name: "App",
    components: {
        Home,
    },
};
</script>

