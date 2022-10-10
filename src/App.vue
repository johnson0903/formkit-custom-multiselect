<script setup>
import { ref } from 'vue'
import { createInput } from '@formkit/vue'
import CustomMultiSelect from './components/CustomMultiSelect.vue'
const cms = createInput(CustomMultiSelect)
const values = ref({})
</script>

<template>
  <main>
    <FormKit v-model="values" :type="cms" label="One-time password" name="two_factor_code"
      help="We’ve sent a code to your phone." validation="required" validation-visibility="live" />
  </main>
</template>
