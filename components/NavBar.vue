<template>
  <div>
    <nav class="navbar navbar-dark bg-dark navbar-expand-lg">
      <a href="/" aria-current="page" target="_self" class="navbar-brand nuxt-link-exact-active nuxt-link-active" >
        <div>
          <img alt="" class="img-fluid lazyLoad" :src="dataNav.url">
        </div>
      </a>
      <button type="button" aria-label="Toggle navigation" id="navbar-collapse" class="navbar-toggler collapsed button-overflow" aria-expanded="false" aria-controls="nav-collapse">
      <span class="navbar-toggler-icon"></span>
      </button>
        <div id="nav-collapse" class="navbar-collapse collapse d-none">
          <ul class="navbar-nav ml-auto header__linksContainer" >
            <li v-for="(item, index) in dataNav.page_links" :key="index" class="nav-item header__linksContainer__link" >
              <a href="/#" target="_self" class="nav-link text-uppercase" >
                {{ item.title }}
              </a>
            </li>
            <div>
              <a href="/kontakt" class="btn button header__Button pdd">
                {{ dataNav.button }}
              </a>
            </div>
          </ul>
      </div>
    </nav>
  </div>
</template>
<script>
import DataNav from '~/api/m2-payload-shared'
export default {
  data () {
    return {
      dataNav: DataNav.section_navbar.image
    }
  }
}
</script>