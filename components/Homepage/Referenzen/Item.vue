<template lang="">
  <div class="Referenzen__card p-sm-4 p-3 text-center text-sm-left">
    <div class="Referenzen__card__img">
      <img alt="car" class="img-fluid rounded-circle lazyLoad isLoaded" :src="image">
    </div>
    <div class="Referenzen__card__price">
      <p>{{ price }}</p>
    </div>
    <div class="Referenzen__card__model">
      <p>{{ title }}</p>
    </div>
    <div class="Referenzen__card__text">
      <p>{{ description }}</p>
    </div>
    <div class="Referenzen__card__clientName">
      <p>{{ subtitle }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    image: {
      type: String
    },
    price: {
      type: String
    },
    title: {
      type: String
    },
    description: {
      type: String
    },
    subtitle: {
      type: String
    }
  }
}
</script>