<template>
<div class="w-1/2 mx-auto">
    <img :src="review.image" />
    <h1 class="text-5xl mb-8">{{review.title}}</h1>
    <p class="mb-8">{{review.description}}</p>
    <nuxt-content :document="review"></nuxt-content>
</div>
</template>
<script>
export default {
    async asyncData({$content, params}) {
        
        let review = await $content('reviews/review'+params.id).fetch()
        console.log(review)
        return {
            review
        }
    },
}
</script>