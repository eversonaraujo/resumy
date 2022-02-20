<template>
    <div class="absolute right-10 top-5 bg-indigo-700  p-3 rounded-lg shadow-lg">
        <div class="flex gap-5">
            <router-link to="/" class="hover:grayscale-0" :class="{'grayscale': $route.path == '/en' }">
                <img src="assets/icons/brasil.png" />
            </router-link>
            <router-link to="/en" class="hover:grayscale-0" :class="{'grayscale': $route.path != '/en' }">
                <img src="assets/icons/eua.png" />
            </router-link>
        </div>
    </div>
</template>

// <script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    props: {
        title: '',
    }
})
</script>
