<template>
  <div class="gallery">
        <b-container>
            <header class="gallery__header">Event Gallery</header>
            <div class="gallery__slider">
                <swiper
                    ref="mySwiperRef"
                    class="horizontal-swiper"
                    :options="swiperOptions"
                    
                >
                    <swiper-slide 
                        v-for="item in items" 
                        :key="item.id"
                    >
                        <div class="gallery__slider__item">
                            <img 
                                :src="require(`../../assets/images/${item.image}`)" 
                                :alt="item.title"
                            />
                        </div>
                    </swiper-slide>
                </swiper>
            </div>
        </b-container>
    </div>
</template>

<script>
import 'swiper/css/swiper.css';
import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
export default {
    name:'CGallery',

    data() {
        return {
            swiperOptions: {
                    loop: true,
                    spaceBetween: 15,
                    slideToClickedSlide: true,
                    slidesPerView:5,
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    },
                    breakpoints: {
                        1024: {
                            slidesPerView: 5,
                        },
                        768: {
                            slidesPerView: 3,
                        },
                        320: {
                            slidesPerView: 2,
                        }
                    }
                }
        }
    },

     components: {
        Swiper,
        SwiperSlide
    },

    props: {
        /**
         * Items
         */
        items:Array,
    },
}
</script>

<style>

</style>