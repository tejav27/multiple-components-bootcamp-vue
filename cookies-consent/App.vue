<template>
  <div>
    <p>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Culpa voluptate
      facere totam in minus placeat, magni architecto voluptatem ipsam quia
      deleniti dolorem quisquam modi at dolore odio minima beatae iure?
    </p>
    <section v-if="displayConsent">
      Please approveeeee !!!! Lorem ipsum dolor sit amet consectetur adipisicing
      elit. Impedit, ipsam tempora quaerat magni eveniet sed repudiandae
      necessitatibus doloribus veniam eligendi.
      <button v-on:click="saveName">Agree</button>
      <button>Disagree</button>
    </section>
  </div>
</template>

<script>
export default {
  mounted() {
    setTimeout(() => {
      console.log(localStorage.consent)
      console.log(!localStorage.consent)
      if (localStorage.consent) {
        this.showconsent = false;
      }
    }, 2000);
  },
  computed:{
    displayConsent() {
      if (localStorage.consent) {
        return false;
      }

      return true;
    }
  },
  methods: {
    saveName() {
      localStorage.consent = true;
      this.showconsent = false;
    },
  },
};
</script>

<style>
</style>