<template>
    <VueMultiselect v-model="props.context._value" :options="options" @select="handleInput">
    </VueMultiselect>
</template>
<script setup>
import VueMultiselect from 'vue-multiselect'
const props = defineProps({
    context: Object,
})
const options = [
    'Monaco',
    'Vatican City',
    'Maldives',
    'Tuvalu',
]
function handleInput(e) {
    props.context.node.input(e)
}
</script>
<style src="vue-multiselect/dist/vue-multiselect.css"></style>