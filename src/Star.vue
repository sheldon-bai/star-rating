<script>
export default {
  name: 'Star',
  computed: {
    fillClass() {
      if (this.id <= this.selectedStar) {
        return 'filled'
      }

      return 'blank'
    }
  },
  props: {
    id: {
      type: Number
    },
    selectedStar: {
      type: Number,
    }
  },
}
</script>

<template>
  <span
    :class="fillClass"
  >*</span>
</template>

<style>
  .filled {
    color: red;
  }

  .blank {
    color: orange;
  }
</style>
