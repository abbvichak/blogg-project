<template>
  <div class="flex flex-wrap justify-center bg-gray-500">
    <div @click="goToReview(review.id)" class="w-80 m-4" v-for="review in reviews" :key="review.id">
      <ReviewListItem :item="review"></ReviewListItem>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$content}) {
    let reviews = await $content('reviews').limit(4).without(['body']).fetch()
    return {
      reviews
    }
  },
  methods: {
    goToReview(id) {
      this.$router.push('/Reviews/'+id)
    }
  }
}
</script>