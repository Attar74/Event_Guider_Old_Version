<template>
  <div>
    <carousel :items-to-show="1"  :autoplay="4000">
      <slide v-for="img in images" :key="img">
        <img class="bg-gray-300 carousel__item block w-full h-full" :src="img" alt="First slide" />
        <div class="overlay w-full">
          <h1 class="text-5xl w-1/2 leading-snug text-white p-5">
            FIND YOUR BEST ORGANIZATION FOR EVENTS, WEDDINGS & PARTIES
            <p class="text-2xl w-2/3">
              The Fastest Way To Discover Top Venues And Services In Egypt To Design And Produce Your Own Events, Weddings And Parties.
            </p>  
          </h1>
        </div>
      </slide>

      <template #addons>
        <navigation />
        <pagination />
      </template>
    </carousel>
  </div>
</template>
  
<script setup>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import { reactive } from 'vue'

const images = reactive([
  "https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg",
  "https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg",
  "https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg",
])
</script>

<style>
.carousel__item {
  min-height: 200px;
  max-height: 655px;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  display: none;
}

.carousel__viewport>ol>li {
  padding: 0px !important;
}

ol.carousel__pagination {
  position: absolute;
  bottom: 10px;
  left: 46%;
}
.carousel__pagination-button::after {
  background-color: white;
  width: 20px;
  height: 2px;
}
.overlay {
  position: absolute; 
  bottom: 0;
  height: 90vh;
  background: rgb(0, 0, 0);
  background: rgba(0, 0, 0, 0.3); /* Black see-through */
  width: 100%;
  transition: .5s ease;
}
.overlay h1 {
  position: absolute;
  top: 22%;
  left: 8%;
  text-align: left;
}
</style>

  