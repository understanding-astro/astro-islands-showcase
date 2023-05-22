<script>
export default {
  data() {
    // data properties used in the UI template
    return {
      upvoteCount: 0,
      maxUpvoteCount: 50,
    };
  },
  methods: {
    // method called when you click the upvote button
    upvote() {
      if (this.upvoteCount < this.maxUpvoteCount) {
        this.upvoteCount++;
      }
    },
  },
};
</script>

<template>
  <div>
    <button @click="upvote">Upvote</button>
    <div>
      <div>Vue</div>

      <div>{{ `${upvoteCount} upvotes` }}</div>
      <div :style="{ width: `${upvoteCount}%` }" />
      <div v-if="upvoteCount === maxUpvoteCount">Max upvote reached</div>
    </div>
  </div>
</template>
