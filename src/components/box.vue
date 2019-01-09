<template>
  <div class='box'>
    <h2>{{data.title}}</h2>
    <p class="box-content">{{data.description}}</p>
    <p class="sub-content"><slot></slot></p>
  </div>
</template>

<script>
export default {
  name: 'box',
  props: ['data'],
  data () {
    return {}
  }
}
</script>

<style lang="scss" scoped>
// @import '@/assets/styles/_color.scss';
// @import '@/assets/styles/_mixin.scss';
.box {
  @include box-shadow;
  @include box(300px, 300px);
}
@media (max-width: 1000px) {
  .box {
    @include box-smartphone(260px, 320px);
  }
}
h2 {
  @include box-title;
}
.box-content {
  @include box-content;
}
.sub-content {
  @include box-sub-content;
}
</style>
