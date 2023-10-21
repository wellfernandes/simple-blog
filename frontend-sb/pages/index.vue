<template>
  <div class="w-1/2 mx-auto my-20">
    <h1 class="text-3xl font-semibold text-red-600">Blog Title</h1>
    <article class="my-20">
      <h2 class="text-5xl font-semibold mb-5">Article Title</h2>
      <p class="mb-5">Article Summary</p>
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
}
</script>
