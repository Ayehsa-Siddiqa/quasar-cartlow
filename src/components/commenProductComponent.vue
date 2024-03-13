<template>
<div class="relative-position q-px-lg">
     <div class="justify">
        <span class="text-h6 q-mr-auto">{{productObj.title}}</span> 
        <q-btn flat icon-right="keyboard_double_arrow_right" label="see all" no-caps href="https://quasar.dev/vue-components/button#progress-related"/>  
    </div>
    <Carousel v-bind="settings" :breakpoints="breakpoints">
        <Slide v-for="(slide, index) in product2Arr" :key="slide">
            <div class="carousel__item bg-white q-ma-sm">
                <q-card class="my-card text-left q-py-sm">
                    <div class="setImg q-px-md">
                        <q-img class="img" :src="slide.productImg" width="100%" height="100%" fit="contain"/> 
                    </div>
                    <q-card-section class="text-black">
                        <div class="fs-13 ellipsis-2-lines">{{slide.nameOfProduct}}</div>
                        <div class="fs-10 text-grey q-py-sm">Condition: {{slide.condition}}</div>
                        <div class="fs-15 q-pa-none q-ma-none">{{slide.currency}}</div>
                        <span class="q-pa-none q-ma-none fs-10 text-grey">{{slide.mainPrice}}</span>
                        <span class="fs-10 text-green">{{slide.discount}}</span>
                        <div class="fs-10 text-red">{{slide.delivery}}</div>
                    </q-card-section>
                </q-card>
            </div>
        </Slide>
        <!-- custom navigation icon -->
        <template #addons="{ slidesCount, currentSlide }">
            <navigation>
                <template #next v-if="currentSlide === slidesCount -1 ">
                    <q-icon name="chevron_right" class="text-black" />
                </template>
                <template #prev v-if="currentSlide > 0">
                    <q-icon name="chevron_left" class="text-black" />
                </template>
            </navigation>
        </template>
    </Carousel>
</div>
</template>

<script>
import {
    defineComponent
} from 'vue'
import {
    Carousel,
    Navigation,
    Slide
} from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'
export default defineComponent({
    name: 'Breakpoints',
    components: {
        Carousel,
        Slide,
        Navigation,
    },
    props: {
        product2Arr: Array,
        productObj:Object
    },
    data: () => ({
        // carousel settings
        settings: {
            itemsToShow: 1,
            snapAlign: 'center',
        },
        // breakpoints are mobile first
        // any settings not specified will fallback to the carousel settings
        breakpoints: {
            // 700px and up
            200:{
                itemsToShow: 2,
                snapAlign: 'center',
            },
            500: {
                itemsToShow: 3,
                snapAlign: 'center',
            },
            800: {
                itemsToShow: 4,
                snapAlign: 'center',
            },
            // 1024 and up
            1024: {
                itemsToShow: 6,
                snapAlign: 'start',
            },
        },
    }),
})
</script>

<style lang="scss">
.setImg {
    width: auto;
    height: 23vh; 
}

.my-card {
    border: 2px solid white;
}

.my-card:hover {
    border: 2px solid black;
}

.carousel__prev,
.carousel__next {
    border: 0px;
    background-color: rgb(184, 174, 174);
    border-radius: 50%;
}

.carousel__prev {
    margin-left: -10px;
}

.carousel__next {
    margin-right: -10px;
}
.justify{
    display: flex; 
    justify-content: space-between;
}
 
</style>
