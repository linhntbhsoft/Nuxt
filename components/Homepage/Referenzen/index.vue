<template>
  <div class="Referenzen">
    <div class="container">
      <h2 class="Referenzen__heading text-center">
        {{ itemReferenzen.title }}
      </h2>
      <p class="Referenzen__text text-center">
        {{ itemReferenzen.subtitle }}
      </p>
      <div class="position-relative"> 
        <b-container>  
          <b-carousel controls @sliding-start="onSlideStart" @sliding-end="onSlideEnd">
            <b-carousel-slide v-for="(count, id) in itemReferenzen.referenzen" :key="id">
              <template v-slot:img>
                <b-row>
                  <b-col cols="12" md="4" sm="4" :class="`${idx < 3 + id && idx >= id ? '' : 'd-none'} mb-3 px-1`" v-for="(slug, idx) in itemReferenzen.referenzen" :key="idx">
                    <Item v-if="idx < 3 + id && idx >= id" :image="slug.image.url" :price="slug.price" :title="slug.title"  :description="slug.description" :subtitle="slug.subtitle" />
                  </b-col>
                </b-row>
              </template>
          </b-carousel-slide>
          </b-carousel>
        </b-container>
      </div>
    </div>
  </div>
</template>
<script>
import Item from './Item'
import DataReferenzen from '~/api/m2-payload-home'
export default {
  components: {
    Item
  },
  data() {
    return {
      itemReferenzen: DataReferenzen.section_referenzen,
      sliding: null
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    }
  }
}
</script>
<style>
.carousel-control-prev {
  background: #e1e1e1;
  transform: translateX(-35px)!important;
  width: 25px;
  height: 25px;
  margin: auto;
}
.carousel-control-next {
  background: #e1e1e1;
  transform: translateX(35px)!important;
  width: 25px;
  height: 25px;
  margin: auto;
}
</style>