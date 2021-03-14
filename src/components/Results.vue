<template>
  <p>زمان کلیک - {{ score }} میلی ثانیه</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank : null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'عالی بود 💪🏻😍'
    } else if (this.score < 400) {
      this.rank = 'خوب بود  👍🏻'
    } else {
      this.rank = 'افتضاح 😂'
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>