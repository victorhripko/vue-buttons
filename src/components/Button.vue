<template>
  <button
    class="btn"
    :class="{
      [`btn--${color}`]: color,
      [`btn--${size}`]: size,
      [`btn--${variant}`]: variant,
      'btn--disable-shadow': disableShadow
    }"
    :disabled="disabled ? disabled : null"
    :tabindex="disabled ? -1 : null"
    type="button"
    @click="onClick"
  >
    <i v-if="startIcon" class="material-icons material-icons--start">
      {{startIcon}}
    </i>
    <slot />
    <i v-if="endIcon" class="material-icons material-icons--end">
      {{endIcon}}
    </i>
  </button>
</template>

<script>
import './_Button.scss';

export default {
  name: 'Button',
  props: {
    variant: {
      type: String,
      validator(value) {
        return ['outline', 'text'].indexOf(value) !== -1;
      },
    },
    disableShadow: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    size: {
      type: String,
      validator(value) {
        return ['sm', 'md', 'lg'].indexOf(value) !== -1;
      },
    },
    color: {
      type: String,
      validator(value) {
        return ['default', 'primary', 'secondary', 'danger'].includes(value);
      },
    },
    startIcon: {
      type: String,
    },
    endIcon: {
      type: String,
    },
  },
  methods: {
    onClick(evt) {
      this.$emit('onClick', evt);
    },
  },
};
</script>
