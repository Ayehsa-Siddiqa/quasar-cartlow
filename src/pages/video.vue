<template>
<q-page padding>
    <vCarousel :navigation="true" :pagination="true" :startAutoPlay="true" :timeout="5000" class="carousel" v-slot="{ currentSlide }">
        <videoCompo v-for="(slide, index) in carouselSlides" :key="index">
            <div v-show="currentSlide === index + 1" class="slide-info">
                <img :src="slide" alt="">
            </div>
        </videoCompo>

    </vCarousel>
</q-page>
</template>

<script>
import vCarousel from 'src/components/vCarousel.vue';
import videoCompo from 'src/components/videoCompo.vue';
export default {
    components: {
        vCarousel,
        videoCompo,
    },
    setup() {
        const carouselSlides = [
            "src/assets/img1.webp",
            "src/assets/img2.webp",
            "src/assets/img3.webp",
            "src/assets/img4.webp",
            "src/assets/img5.webp",
            "src/assets/img6.webp"
        ];
        return {
            carouselSlides
        }

    }
}
</script>

<style lang="scss" scoped>
.carousel {
    max-height: 50vh;
    height: 55vh;
    position: relative;
    
.slide-info {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  max-height: 100%;
  height: 100%;
  
}
}

</style>
