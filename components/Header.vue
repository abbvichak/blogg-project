<template>
    <div class="bg-gray-400">
        <nav class="flex items-center justify-between flex-wrap bg-teal-500 p-6">
            <div class="flex items-center flex-shrink-0 mr-6">
                <svg class="fill-current h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54" ></svg>
                <span class="font-semibold text-xl tracking-tight">Game Reviews</span>
            </div>
              <div class="block lg:hidden" id="menu">
                <button class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white">
                <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
                </button>
            </div>
            <div class="float-right">
                <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
                    <div class="text-sm lg:flex-grow">
                        <nuxt-link to="secrets" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 mr-4 text-gray-400">
                        Secrets
                        </nuxt-link>
                        <nuxt-link to="/" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
                        Home
                        </nuxt-link>
                        <nuxt-link to="reviews" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
                        Reviews
                        </nuxt-link>
                        <nuxt-link to="/merch" target="empty" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
                        Merch
                        </nuxt-link>
                        <nuxt-link to="about-me" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
                        About Me
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
toggle() {

    let open = document.getElementById("menu")

    open.classList.toggle("hidden")

},
mounted() {

    let recaptchaScript = document.createElement('script')

    recaptchaScript.setAttribute('src', 'https://www.google.com/recaptcha/api.js')

    document.head.appendChild(recaptchaScript)

},

}
</script>

<style>

</style>