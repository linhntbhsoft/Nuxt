<template>
  <div class="col-xl-6 col-12 px-xl-0">
    <div class="auto__content__container1">
      <div class="auto__content">
        <h2 class="auto__content__heading text-xl-left text-center">
           {{ title }}
        </h2>
        <h2 class="auto__content__subheading text-xl-left text-center">
          Wir übernehmen für Sie
        </h2>
      <div class="auto__content__bulletsbuttonsContainer">
        <div class="auto__content__bullet" v-for="(item, index) in listBullet" :key="index">
          <div class="d-flex bullet  auto__content__bullet__bulletText">
            <div class="bullet__imgContainer">
              <img alt="" class="img-fluid lazyLoad isLoaded" :src="image">
            </div>
            <div class="ml-2 bullet__textContainer">
              <p class="bullet__text"> {{ item.title }}</p>
            </div>
          </div>
        </div>
      <div class="d-flex flex-sm-row justify-content-center justify-content-sm-start flex-column w-100 auto__content__buttonPriceContainer">
        <div class="auto__content__buttonPriceContainer__box1">
          <a href="/kaufen" class="btn button auto__content__buttonPriceContainer__box1__button autosuchenBtn">
           {{ button }}
          </a>
        </div> 
        <div v-if="price" class="auto__content__price"><div class="auto__content__tag">
          <img alt="" class="lazyLoad isLoaded" src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/2wBDAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/wAARCAAZAGsDASIAAhEBAxEB/8QAFwABAQEBAAAAAAAAAAAAAAAAAAkLCP/EACYQAAEEAgIABQUAAAAAAAAAAAQAAwUGAgcBCAkSExQVChE3hrb/xAAYAQEAAwEAAAAAAAAAAAAAAAAACAkKB//EACQRAAEEAgEEAgMAAAAAAAAAAAMAAgQFAQYHCBESEwkVFBYh/9oADAMBAAIRAxEAPwCJ6Iir/W3hERERERERERERERERERERdPdP+p+z+6W96jonVYf2lJ57k6x2QoZ9+EolNBeHxn7nYcmOcecI6KaIZaHH9Vl2XmC4yCCc+QlBcctELRvQbqlojUlC1FA6V1tZ4+jQLETzZrvRKnZ7bZZDN546ZsNgmpWIKKJkpyYMPlCGGnGo2P5L4jYYOPiBAQBp1/T96z601npeJf8ATcwNadr3qXzZ7BzR4o4lnrlvh+XPjdd5iYuPPg1WAjDG5SuO+u43YvmzLJn7Z6QyiIe7ilTxjpsCqpQ20hsadYXEcZ8lxgZxRoj/ABIKIF2fJuX98YfLe3t3M1ov60DXOza/Ib1W7pyRyzacZUZNg0/SOLLqdVDrnum0tnsGzxfZDsNktI+Mx5DImBuLF1qOby8aoxbPOBluCx4+SuiIorLSUiIiIiIiIiIiIiIiIiIiIqAeHJ33v/QHfkZsaB5NnNb2XkKv7j15gR5BbfUPc85e8CadzxGHt9XzeflapKZctZtE8lw5T/EJOTI5OjJqXa+v9561pm3dWWQG3a/v8GLYaxPx+WXpGAk+bBxkhhzHAmPlI0tomLmog5oeShZgI6JkxRZAIkdrKbVmOqP4BoX7T/aWNda433efR4lVJA/n1+RvlRwvPkLop/YJhPST1G7BNh+XPD4YbguPYzLXPL7KxevzpA03mB2t8lQbX9M3cc6Prd3axacdrH2So+vnyYH2kPFhVOdZ1ToTY8KzxJcV1cZ0CUOQGLW5g//Z">
          <p class="auto__content__tag__text">PREIS</p>
          </div> 
          <h5 class="auto__content__tag__price"> {{ price }}</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  props: {
    image: {
      type: String
    },
    title: {
      type: String
    },
    button: {
      type: String
    },
    listBullet: {
      type: Array
    },
    price: {
      type: String
    }
  }
}
</script>
