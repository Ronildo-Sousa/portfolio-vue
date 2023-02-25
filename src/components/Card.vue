<script>
import MyButton from './MyButton.vue'
export default {
    props: {
        image: String,
        title: String,
        description: String,
        link: String,
        link_text: String,
    },
    components: {
        MyButton
    }
}

</script>

<template>
    <div class="w-[400px] max-w-sm px-4 mx-auto lg:max-w-md">
        <div
            class="overflow-hidden bg-gray-900 rounded-lg cursor-pointer bg-gradient-to-b from-gray-700 to-gray-900 hover:from-gray-900 hover:to-gray-700">
            <div class="">
                <img class="w-full rounded " :src="image ?? 'https://picsum.photos/seed/picsum/400/300'"
                    alt="card-item">
            </div>
            <div class="flex flex-col items-center p-6">
                <h1 class="mb-3 text-xl font-medium">{{ title }}</h1>
                <p class="mb-3 break-words">
                    {{ description }}
                </p>
                <MyButton :uri="link">
                    {{ link_text }}
                </MyButton>
            </div>
        </div>
    </div>
</template>