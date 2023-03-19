<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { EffectCube, Pagination } from 'swiper'

import 'swiper/css/effect-cube'
import 'swiper/css/pagination'
import "swiper/css"
const props = defineProps({
    photots: {
        required: true
    }
})
</script>

<template>
    <div class=" text-center">
        <h1>a simple carousel for vue js with swiper</h1>
        <Swiper :modules="[EffectCube, Pagination]" effect="cube" :cubeEffect="{
            shadow: true,
            slideShadows: true,
            shadowOffset: 20,
            shadowScale: 0.95
        }" :grabCursor="true" :loop="true" :pagination="true">
            <SwiperSlide v-for="photo in props.photots" :key="photo">
                <img :src="`${photo}`" alt="">
            </SwiperSlide>
        </Swiper>
    </div>
</template>

<style>
.swiper {
    width: 500px;
    height: 500px;
    overflow: hidden;
}

.swiper-slide img {
    width: 100%;
    height: 100%;
}

.text-center {
    text-align: center;
}
</style>
