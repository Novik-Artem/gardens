<template>
  <div>
    <FullScreen id="main" />
    <About id="about" />
    <Matters />
    <Solution id="solution" />
    <Needs />
    <Start id="start" />
    <Points />
    <!-- <Impact id="impact" /> -->
    <!-- <Support id="support" /> -->
    <!-- <BrownCards /> -->
    <Development id="development" />
    <Activities id="resources" />
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
import Needs from "./components/Needs.vue";
import Points from "./components/Points.vue";
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
    Needs,
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
