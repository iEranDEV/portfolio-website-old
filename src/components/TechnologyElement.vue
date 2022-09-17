<template>
    <div class="w-full flex items-center flex-col">
        <p class="text-xl md:text-3xl">
            <slot></slot>
        </p>
        <p class="text-sm md:text-lg text-lime">{{ name }}</p>
        <div class="flex items-center">
            <i v-for="index in 5" :key="index" class="fa-regular fa-star text-stone-400 text-xs md:text-md" :class="{'font-bold text-orange-300': stars >= index}"></i>
        </div>
    </div>
</template>

<script>

export default {
    props: {
        name: String,
        stars: Number
    }
}
</script>

<style>

</style>