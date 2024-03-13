<template>
<div class="carousel">
    <slot :currentSlide="currentSlide" />
    <!-- navigation -->
    <div v-if="navEnabled" class="navigate">
        <div class="toggle-page left">
            <q-icon name="chevron_left" @click="prevSlide" style="font-size: 40px;" class="text-white hoverable-up-5" />
        </div>
        <div class="toggle-page right">
            <q-icon name="chevron_right" @click="nextSlide" style="font-size: 40px;" class="text-white hoverable-up-5" />
        </div>
    </div>

    <!-- pagination -->
    <div v-if="paginationEnabled" class="pagination">
        <span v-for="(slide, index) in getSlideCount" :key="index" @click="goToSlide(index)" :class="{ active: index+1 === currentSlide}">
        </span>
    </div>
</div>
</template>

<script>
import {  ref, onMounted } from 'vue'
export default {
    props: ['startAutoPlay', 'timeout', 'navigation', 'pagination'],
    setup(props) {
        const currentSlide = ref(1);
        const getSlideCount = ref(null);
        const autoPlayEnabled = ref(props.startAutoPlay === undefined ? true : props.startAutoPlay);
        const timeOutDuration = ref(props.timeout === undefined ? 5000 : props.timeout);
        const paginationEnabled = ref(props.pagination === undefined ? true : props.pagination);
        const navEnabled = ref(props.navigation === undefined ? true : props.navigation);

        // next slide
        const nextSlide = () => {
            if (currentSlide.value === getSlideCount.value) {
                currentSlide.value = 1;
                return;
            }
            currentSlide.value += 1;
        }
        // prev slide 
        const prevSlide = () => {
            if (currentSlide.value === 1) {
                currentSlide.value = 1;
                return;
            }
            currentSlide.value -= 1;
        }

        // goto slide 
        const goToSlide = (index) => {
            currentSlide.value = index + 1;
        }
        // autoplay 
        const autoPlay = () => {
            setInterval(() => {
                nextSlide()
            }, timeOutDuration.value)
        }
        if (autoPlayEnabled.value) {
            autoPlay();
        }

        onMounted(() => {
            getSlideCount.value = document.querySelectorAll('.slide').length;
        })
        return {
            currentSlide,
            nextSlide,
            prevSlide,
            getSlideCount,
            goToSlide,
            paginationEnabled,
            navEnabled,
        }
    }
}
</script>

<style lang="scss" scoped>
.navigate {
    width: 100%;
    height: 100%;
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;

    .toggle-page {
        display: flex;
        flex: 1;
        margin-left: -20px;
    }

    .right {
        justify-content: end;
        margin-right: 20px;
    }

    i {
        cursor: pointer;
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: grey;
    }
}

.pagination {
    width: 100%;
    position: absolute;
    bottom: 0;
    margin-bottom: -60px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 16px;

    span {
        width: 15px;
        height: 5px;
        border-radius: 5px;
        background-color: grey;
        cursor: pointer;
    }

    .active {
        background-color: black;
    }
}
</style>
