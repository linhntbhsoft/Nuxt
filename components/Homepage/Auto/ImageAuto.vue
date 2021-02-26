<template>
  <div class="col-xl-6 d-xl-block d-none px-xl-0 auto__col">
    <img alt="" class="img-fluid auto__content__image w-100 lazyLoad isLoaded"  :src="image">
  </div>
</template>
<script>
export default {
  props: {
    image: {
      type: String
    }
  }
}
</script>
<style scoped>
.auto__content__image{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  -o-object-fit: cover;
  object-fit: cover;
}
</style>