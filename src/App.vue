<template>
  <div>
    <FullScreen />
    <About />
    <Matters />
    <Solution />
    <Points />
  </div>
</template>

<script>
import About from "./components/About.vue";
import FullScreen from "./components/FullScreen.vue";
import Matters from "./components/Matters.vue";
import Solution from "./components/Solution.vue";
import Points from "./components/Points.vue";
export default {
  components: {
    FullScreen,
    About,
    Matters,
    Solution,
    Points,
  },
};
</script>
