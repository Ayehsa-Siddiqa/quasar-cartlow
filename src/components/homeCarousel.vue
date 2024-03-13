<template>
  <Carousel :autoplay="2000" :items-to-show="1" :wrap-around="false">
    <Slide v-for="slide in homeCarousel" :key="slide">
      <div class="carousel__item overflow-hidden">  
          <img :src="slide" width="100%" class="rounded-borders"/>
      </div>
    </Slide> 
    <template #addons>
        <Pagination />
        <Navigation />
    </template> 
  </Carousel>
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Pagination, Slide,Navigation } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  name: 'Autoplay',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
   props:{
    homeCarousel:Array,
   }
})
</script>


 

 