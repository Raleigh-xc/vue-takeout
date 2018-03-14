<template>
  <div class="star" :class="starType">
    <span class="star-item" v-for="itemClass in itemClasses" :class="itemClass"></span>
  </div>
</template>
<script>
export default {
  props: {
    size: {
      type: Number
    },
    score: {
      type: Number
    }
  },
  computed: {
    starType() {
      return 'star-' + this.size;
    }
  }
}
</script>
<style lang="stylus">
  .star
    font-size 0
    .star-item
      display inline-block
      background-repeat no-repeat
    &.star-48
      .star-item
        width 20px
        height 20px
    &.star-36
      .star-item
        width 20px
        height 20px
    &.star-34
      .star-item
</style>


