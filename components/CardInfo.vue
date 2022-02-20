<template>
    <div class="mt-5">
        <h2 class="text-xl">{{ title }}</h2>
        <ul class="text-gray-100 mt-1">
            <li v-for="item, index in items" :key="index" v-html="item"></li>
        </ul>
    </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    props: {
        title: { type: String , default: '' },
        items: { type: Array, default: [] }
    }
})
</script>
