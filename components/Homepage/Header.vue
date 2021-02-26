<template>
  <div class="home" :style="{'background-image': 'url(' + dataHeader.background_image.url + ')'}">
    <div class="d-flex flex-column">
      <div class="home__logo text-center">
        <div class="text-center">
          <img alt="" class="img-fluid lazyLoad" :src="dataHeader.image.url">
          <h1 class="home__logo__text text-center">
            {{ dataHeader.title }}
          </h1>
        </div>
      </div>
      <div class="home__content text-center">
        <h2 class="home__content__text">
          {{ dataHeader.subtitle }}
        </h2>
      <div class="home__content__buttons">
        <div class="home__content__buttons__container d-flex flex-sm-row flex-column text-center justify-content-center align-items-center">
          <a href="/kaufen" class="btn button home__content__buttons__button__redButton pd-button text-uppercase">
            {{ dataHeader.button_1 }}
          </a>
          <a href="/verkaufen" class="home__content__buttons__button__blue text-uppercase">
            {{ dataHeader.button_2 }}
          </a>
        </div>
      </div>
    </div>
  </div>
  </div>
</template>
<script>
import DataHome from '~/api/m2-payload-home'
export default {
  data () {
    return {
      dataHeader: DataHome.section_head
    }
  }
}
</script>
<style scoped>
  .pd-button {
    padding:18px 60px;
    margin-right:30px;
  }
</style>