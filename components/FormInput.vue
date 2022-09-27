<template>
  <div class="FormInput">
    <label
      :for="$attrs.id"
      class="FormInput__label"
    >
      {{ label }}
    </label>
    <input
      v-bind="$attrs"
      :type="$attrs.type || 'text'"
      :autocomplete="$attrs.autocomplete || 'off'"
      :value="value"
      :aria-label="label"
      class="FormInput__input"
      @input="updateValue"
    >
  </div>
</template>

<script>
import FormMixin from '~/mixins/FormMixin';

export default {
  name: 'FormInput',

  mixins: [FormMixin],

  props: {
    value: {
      type: String,
      default: '',
    },
  },
};
</script>

<style lang="postcss" scoped>
.FormInput__label {
  font-weight: 600;
  color: var(--color-white);

  @media (--laptop) {
    font-size: 3rem;

    &:hover {
      cursor: pointer;
    }
  }
}

.FormInput__input {
  border-bottom: 1px solid var(--color-white);
  width: 100%;

  &::placeholder {
    opacity: 0.75;
  }
}
</style>
