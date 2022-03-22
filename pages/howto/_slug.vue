<template>
  <div>
    <nuxt-content class="artical-content prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto" :document="post" />
  </div>
</template>

<script>
export default {
  name: 'HowToSlug',
  async asyncData({ $content, params, app, error }) {
    console.log(params);
    const post = await $content(app.i18n.locale, 'howto', params.slug)
      .fetch()
      .catch(() => {
        error({ statusCode: 404, message: 'Page not found' })
      })
    return { post }
  },
}
</script>

<style lang="scss">
@media screen and (max-width: 767px) {
  .artical-content {
    padding:20px;
  }
}

</style>
