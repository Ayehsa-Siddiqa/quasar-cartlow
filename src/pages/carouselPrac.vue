<template>
 <div class="row">
     <div class="col-10">
      <Carousel v-bind="settings" :breakpoints="breakpoints">
        <Slide  v-for="slide in  carouselArr" :key="slide">
          <div class="carousel__item q-gutter-sm">
            <q-btn no-wrap flat dense :name="slide.label" :label="slide.label" class="fs-12"/>  
          </div>
        </Slide> 
        <template #addons>
          <Navigation />
        </template>
      </Carousel>
     </div>
 </div>
 <!--nav slider end -->
 
</template> 

<script>
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  name: 'Breakpoints',
  components:{
    Carousel,
    Slide,
    Navigation,  
  },
  data: () => ({
    carouselArr:[
        {
          label:"60%-off",
        },
        {
          label:"MOBILES",
        },
        {
          label:"Laptops",
        },
        {
          label:"tablets",
        },
        {
          label:"smartwatches",
        },
        {
          label:"fragrences",
        },
        {
          label:"watches",
        },
        {
          label:"FASHION",
        },
        {
          label:"small appliance",
        },
        {
          label:"cell you old devices",
        },
        {
          label:"VIDEOS",
        },
        {
          label:"ARTICLES",
        } 
    ],
    // carousel settings
    settings: {
      itemsToShow: 1,
      snapAlign: 'center',
    },
    // breakpoints are mobile first
    // any settings not specified will fallback to the carousel settings
    breakpoints: {
      // 700px and up
      700: {
        itemsToShow: 3.5,
        snapAlign: 'center',
      },
      // 1024 and up
      1024: {
        itemsToShow: 8,
        snapAlign: 'center',
      },
    },
  }),
})
</script>



