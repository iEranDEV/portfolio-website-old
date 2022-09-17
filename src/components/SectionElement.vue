<template>
    <section :id="id" class="section">
        <div class="w-4/6 md:w-1/2 mb-6 flex">
            <p class="py-2 text-stone-400 text-xl w-full md:w-1/3">
                <slot name="header">
                    00. Section without name
                </slot>
            </p>
            <div class="w-full">
                <div class="h-1/2 border-b border-stone-300"></div>
                <div class=" h-1/2"></div>
            </div>
        </div>
        <div class="w-4/6 h-1/2 md:w-1/2 pt-2">
            <slot name="content">t</slot>
        </div>
    </section>
</template>

<script>

export default {
    props: {
        id: {
            type: String,
            required: true,
        }
    }
}
</script>

<style>

</style>