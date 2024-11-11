<template>
  <div>
    <FullScreen />
    <About />
    <Matters />
    <Solution />
    <Applicate />
    <Start />
    <Points />
    <Impact />
  </div>
</template>

<script>
import About from "./components/About.vue";
import FullScreen from "./components/FullScreen.vue";
import Matters from "./components/Matters.vue";
import Solution from "./components/Solution.vue";
import Points from "./components/Points.vue";
import Applicate from "./components/Applicate.vue";
import Start from "./components/Start.vue";
import Impact from "./components/Impact.vue";
export default {
  components: {
    FullScreen,
    About,
    Matters,
    Solution,
    Applicate,
    Start,
    Points,
    Impact,
  },
};
</script>
