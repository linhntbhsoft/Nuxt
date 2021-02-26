<template>
  <div>
    <Header />
    <Referenzen />
    <Benefits />
    <div class="auto">
      <div class="row auto__row mx-xl-0 mt-xl-0 mt-4">
        <ContentAuto :image="dataService1.checkbox_image" :title="dataService1.title" :button="dataService1.button" :list-bullet="dataService1.list" :price="dataService1.price" />
        <ImageAuto :image="dataService1.image.url"/>
      </div>
    </div>
    <div class="auto">
      <div class="row auto__row mx-xl-0 mt-xl-0 mt-4">
        <ImageAuto :image="dataService2.image.url"/>
        <ContentAuto :image="dataService1.checkbox_image" :title="dataService2.title" :button="dataService2.button" :list-bullet="dataService2.list" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from '~/components/Homepage/Header'
import Referenzen from '~/components/Homepage/Referenzen'
import Benefits from '~/components/Homepage/Benefits'
import ContentAuto from '~/components/Homepage/Auto/ContentAuto'
import ImageAuto from '~/components/Homepage/Auto/ImageAuto'
import Payload from '~/api/m2-payload-home'
export default {
  components: {
    Header,
    Referenzen,
    Benefits,
    ImageAuto,
    ContentAuto
  },
  data() {
    return {
      dataService1: Payload.section_services.service_1,
      dataService2: Payload.section_services.service_2
    }
  }
}
</script>

<style src="~/assets/css/home.css"></style>
