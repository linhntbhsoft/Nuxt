<template>
  <div class="benefits__content">
    <div class="d-flex align-items-center justify-content-center justify-content-md-start">
      <h4 class="benefits__content__number text-center text-md-left">
        {{ number }}
      </h4>
      <div class="benefits__content__iconbox ml-2">
        <div class="benefits__content__iconbox__icon">
          <img alt="" class="benefits__content__iconbox__icon__img lazyLoad isLoaded" :src="image">
        </div>
      </div>
    </div>
    <h6 class="benefits__content__heading text-center text-md-left">
      {{ heading }}
    </h6>
    <p class="benefits__content__text text-center text-md-left">
      {{ text }}
    </p>
  </div>
</template>
<script>
export default {
  props: {
    number: {
      type: Number
    },
    image: {
      type: String
    },
    heading: {
      type: String
    },
    text: {
      type: String
    }
  }
}
</script>
