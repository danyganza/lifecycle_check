<template>
  <div>
    <p>Hello from the other side</p>
    <div class="script_container"></div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      tweets: [`best day ever`, `second tweet`],
      num_friends: 2,
      logged_in: true,
    };
  },
  methods: {
    show_info: function () {
      let script_container = document.querySelector(".script_container");
      script_container.insertAdjacentHTML(
        `beforeend`,
        `<p>Friends ${this.num_friends}</p>`
      );
      if (this.logged_in === true) {
        script_container.insertAdjacentHTML(
          `beforeend`,
          `<p>you are logged in</p>`
        );
      } else {
        script_container.insertAdjacentHTML(
          `beforeend`,
          `<p>you are Not logged in</p>`
        );
      }
      for (let i = 0; i < this.tweets.length; i++) {
        script_container.insertAdjacentHTML(
          `beforeend`,
          `<p>${this.tweets[i]}</p>`
        );
      }
    },
  },
  mounted: function () {
    this.show_info();
  },
};
</script>

<style scoped>
</style>
