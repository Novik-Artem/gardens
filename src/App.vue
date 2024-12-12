<template>
  <div>
    <FullScreen />
    <About id="about" />
    <Matters />
    <Solution id="solution" />
    <Applicate />
    <Start id="start" />
    <Points />
    <Impact id="impact" />
    <Support id="support" />
    <BrownCards />
    <Development />
    <Activities />
    <Partners id="partners" />
    <Contacts />
    <Footer />
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
import Support from "./components/Support.vue";
import BrownCards from "./components/BrownCards.vue";
import Development from "./components/Development.vue";
import Activities from "./components/Activities.vue";
import Partners from "./components/Partners.vue";
import Contacts from "./components/Contacts.vue";
import Footer from "./components/Footer.vue";
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
    Support,
    BrownCards,
    Development,
    Activities,
    Partners,
    Contacts,
    Footer,
  },
};
</script>
