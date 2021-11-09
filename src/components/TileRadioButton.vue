<template>
  <fieldset>
    <h3>{{ title }}</h3>
    <template v-for="(option, index) in options">
      <label :key="index">
        <input
          type="radio"
          :name="name"
          :value="option.value"
          @change="updateValue"
        />{{ option.label }}
      </label>
    </template>
  </fieldset>
</template>

<script>
export default {
  props: {
    value: { type: String, required: true },
    options: { type: Array, required: true },
    name: { type: String, required: true },
    title: { type: String }
  },
  methods: {
    updateValue: function (e) {
      this.$emit('input', e.target.value)
    }
  }
}
</script>

<style scoped>
label {
  display: block;
}
</style>
