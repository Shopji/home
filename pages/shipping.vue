<template>
  <div>
    <nuxt-content class="prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto" :document="post" />
  </div>
</template>

<script>
export default {
  name: 'Return Policy',
  async asyncData({ $content, params, app, error }) {
    console.log(params);
    const post = await $content(app.i18n.locale, 'shipping')
      .fetch()
      .catch(() => {
        error({ statusCode: 404, message: 'Page not found' })
      })
    return { post }
  },
}
</script>
