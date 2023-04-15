<template>
  <div>
    <button @click="toggle_post">TOOGLE POST</button>
    <article v-if="show_post===true">
    <button @click="hack_post">Hack blog</button>
    <h1>{{ blog_tittle }}</h1>
    <p>{{ blog_content }}</p>
    <img :src="blog_image_url" alt="" />
    </article>
  </div>
</template>

<script>
export default {
    methods: {
        hack_post: function(){
            this.blog_content= this.blog_content +"iwas injected";
        },
        toggle_post: function (){
            this.show_post = !this.show_post
        }
    },
  data() {
    return {
        show_post: false,
      blog_tittle: `Big Blog`,
      blog_content: `Yeah, but John, if The Pirates of the Caribbean breaks down, the pirates don’t eat the tourists. Yeah, but your scientists were so preoccupied`,
      blog_image_url: `https://images.unsplash.com/photo-1542435503-956c469947f6?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1374&q=80`,
    };
  },
};
</script>

<style scoped>
</style>