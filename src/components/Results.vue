<template>
  <p>Reaction Time: {{ score }} ms</p>
  <div>
    <p class="rank">{{ rank }}</p>
  </div>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score <= 250) {
      this.rank = "Ninja Fingers";
    } else if (this.score <= 300) {
      this.rank = "Fast but not quick";
    } else {
      this.rank = "You got frozen fingers?";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: #0faf87;
  font-weight: bold;
}
</style>
