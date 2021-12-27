<template>
  <div>
    <scratch-card
      :key="renderCount"
      :cardWidth="cardWidth"
      :cardHeight="cardHeight"
      :finishPercent="finishPercent"
      imageUrl="https://i.imgur.com/zdFRqJI.png"
      :forceReveal="forceReveal"
      @complete="onComplete"
    >
      <div class="tile-block w-48 h-48"></div>
    </scratch-card>
  </div>
</template>

<script>
import ScratchCard from "vue-scratchcard";
// const onComplete = () => window.alert('Content revealed!');

export default {
  name: "HelloWorld",
  components: {
    ScratchCard
  },
  data() {
    return {
      cards: [
        { score: "1" },
        { score: "2" },
        { score: "3" },
        { score: "4" },
        { score: "5" },
        { score: "6" },
        { score: "7" },
        { score: "8" },
        { score: "9" }
      ],
      renderCount: 0,
      cardWidth: 140,
      cardHeight: 140,
      finishPercent: 100,
      forceReveal: false
    };
  },
  props: {
    msg: String
  },
    methods: {
    onComplete() {
      // `this` will refer to the component instance
      window.alert("Content revealed!");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tile-block {
  background: url("https://i.imgur.com/0D63VBH.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
  height: 140px;
}
</style>
