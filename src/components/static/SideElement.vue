<template>
    <div class="fixed 0 h-screen w-8 md:w-32" :class="{'right-0': right}">
        <slot></slot>
    </div>
</template>

<script>

export default {
    props: {
        right: {
            type: Boolean,
            deafult: false
        }
    }
}
</script>

<style scoped>

</style>