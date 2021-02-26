<template>
  <div class="benefits">
    <div class="container">
      <h3 class="benefits__heading text-center"> {{ itemBenefit.subtitle }}</h3>
      <h2 class="benefits__heading2 text-center">{{ itemBenefit.title }}</h2>
      <div class="row">
        <div class="col-xl-3 col-md-6 col-12 mb-4 mb-md-0" v-for="(item, index) in itemBenefit.vorteile" :key="index">
          <Content :number="index+1" :image="item.image.url" :heading="item.title" :text="item.description" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Content from './Content'
import DataBenefit from '~/api/m2-payload-home'
export default {
  components: {
    Content
  },
  data() {
    return {
      itemBenefit: DataBenefit.section_vorteile
    }
  }
}
</script>