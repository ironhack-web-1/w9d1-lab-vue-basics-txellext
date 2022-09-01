<template>
  <div>
    <input
    :placeholder="placeholder"
    :type="type"
    :name="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>

<script>
export default {
    props: {
        placeholder: {
            type: String,
            default: "text",
        },
        type: {
            default: "text"
        },
        modelValue: {
            type: String,
            required: true,
        },


    }
}
</script>

<style>

</style>