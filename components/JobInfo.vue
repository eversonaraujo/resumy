<template>
    <div class="mt-5 bg-white text-gray-700 p-7 rounded shadow">
        <h2 class="text-xl text-blue-800 mb-3">{{ company }}</h2>
        <p><strong>Role: </strong>{{ role }}</p>
        <p><strong>Activities: </strong>{{ activities }}</p>
        <p><strong>Time: </strong>{{ time }} </p>


        <h2 v-if="projects.length" class="text-xl mt-5 mb-3">Projects</h2>
        <div v-for="p, index in projects" :key="index" class="mt-5 mb-3 border-l-4 pl-5 ">
            <a :href="p.link" target="_blank" 
                class="flex items-center text-md text-gray-900 mb-2 hover:text-blue-700">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" />
                </svg>
                {{ p.name }}
            </a>
            <p>{{ p.architeccture }}</p>
            <p class="text-sm">{{ p.desc }}</p>
        </div>

    </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    props: {
        role: '',
        time: '',
        company: '',
        activities: '',
        projects: { type: Array, default: [] }
    }
})
</script>
