<template>
    <div id="notification" class="w-80 bottom-0 right-0 fixed m-8 rounded-lg p-2 text-stone-100 shadow-lg flex justify-center items-center hidden" :class="positive ? 'bg-green-500' : 'bg-red-500'">
        <p v-if="positive" class="text-stone-100">
            Pomyślnie wysłano wiadomość!
        </p>
        <p v-else class="text-stone-100">
            Nie udało się wysłać wiadomości!
        </p>
    </div>
</template>

<script>

export default {
    props: {
        positive: {
            type: Boolean,
            default: true,
        },
        message: {
            type: String
        }
    }
}
</script>

<style>

</style>