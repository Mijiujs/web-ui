<template>
  <button
    @click="handleClick"
    :disabled="disabled"
    :class="[
        'hyk-button',
        type?'hyk-button--'+type:'',
        size?'hyk-button--'+size:'',
        {
            'plain':plain,
            'round':round,
            'disabled':disabled,
            'circle':circle,
        }
    ]"
  >
    <span v-if="$slots.default">
      <slot></slot>
    </span>
  </button>
</template>
<script>
// const TYPE_LIST = ['default', 'primary', 'success', 'warning', 'error', 'info']
// const SIZE_LIST = [ 'normal', 'small', 'mini']
// const TYPE_COLOR = {
//   default: '#F5F5F5',
//   primary: '#5D82E6',
//   success: '#67c23a',
//   info: '#f56c6c',
//   warning: '#909399',
//   error: '#e6a23c'
// }
export default {
  name: 'hyk-button',
  props: {
    size: {
      type: String,
      default: 'normal'
    },
    type: {
      type: String,
      default: 'default'
    },
    plain: Boolean,
    round: Boolean,
    circle: Boolean,
    loading: Boolean,
    disabled: Boolean
  },
  methods: {
    handleClick (evt) {
      this.$emit('click', evt)
    }
  }
}
</script>
