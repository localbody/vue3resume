<script>
export default {
    name: 'Quotes',
    props: {
        text: {
            type: String,
            required: true,
        }
    }
}
</script>

<template>
    <div class="quotes">{{ text }}</div>
</template>

<style scoped></style>