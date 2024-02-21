<template>
  <div class="w-1/2 mx-auto my-20">
    <h1 class="text-3xl font-semibold text-red-600">{{ this.title }}</h1>
    <article class="my-20">
      <h2 class="text-5xl font-semibold mb-5">{{ this.article.title }}</h2>
      <p class="mb-5">{{ this.article.summary }}</p>
      <p class="text-red-500">Read More</p>
    </article>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'Blog Title',
      article: {
        title: 'Article Title',
        summary: 'Article Summary'
      }
    }
  },

  methods: {
    getArticle () {
      this.$axios.$get('http://localhost:3000/articles/1')
        .then(response => {
          this.article = response.data
        })
        .catch(error => {
          console.log(error)
          alert.error(ERROR_CONSTANTS.GET_ARTICLE_ERROR);
        })
    },
  },

}
</script>

<style scoped>

</style>
