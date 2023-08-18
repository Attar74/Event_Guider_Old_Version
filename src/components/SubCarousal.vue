<template>
  <div class="px-32 pb-16">
    <div class="flex pt-5 pb-5 pl-1 justify-between">
      <h1 class="text-left text-4xl leading-snug text-black">{{ title }}</h1>
      <div class="flex align-center justify-center my-auto">
        <RouterLink class="text-[#20b3fa] mr-2 hover:underline" to="/">See All</RouterLink>
        <button class="mr-2 border-solid border border-black rounded" @click="moveSLider('next')">
          <svg class="p-1.5 w-6 h-6 text-white-800 dark:text-black" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 8 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 1 1.3 6.326a.91.91 0 0 0 0 1.348L7 13"/>
          </svg>
        </button>
        <button class="mr-2 border-solid border border-black rounded" @click="moveSLider('prev')">
          <svg class="p-1.5 w-6 h-6 text-white-800 dark:text-black" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 8 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 13 5.7-5.326a.909.909 0 0 0 0-1.348L1 1"/>
          </svg>
        </button>
      </div>
    </div>
    <carousel ref="myCarousel" class="sub_carousal" v-bind="settings" :items-to-show="4" :autoplay="1000">
      <slide v-for="img in props.images" :key="img">
        <div class="px-5 pt-5 relative">
          <span class="absolute right-10 top-8 bg-white rounded-full cursor-pointer">
            <svg class="p-1 w-[30px] h-[30px] text-gray-800 dark:text-[#20b3fa]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 21 19">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 4C5.5-1.5-1.5 5.5 4 11l7 7 7-7c5.458-5.458-1.542-12.458-7-7Z"/>
          </svg>
          </span>
          <img class="image_rounded-top carousel__item block w-full h-full" :src="img" alt="First slide" />
          <div class="text-left bg-white border-solid border border-gray rounded p-5">
            <h1 class="font-bold mb-2">Steigenberger Tahrir</h1>
            <p class="mb-1 font-light	">
              Offering views of the Nile river, this modern hotel in downtown 
            </p>
            <span class="flex justify-between">
              <span class="flex" v-if="seats">
                <span class="bg-[#f5f5f5] rounded-full">
                  <i class="p-2 fas fa-couch text-[#3e2f2f]" />
                </span>
                <p class="text-[#808285] text-sm my-auto leading-snug ml-1">
                  Seats: 250
                </p>
              </span>
              <span class="flex align-center">
                <svg class="my-auto w-[15px] h-[15px] text-gray-800 dark:text-[#20b3fa]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 16 20">
                  <path d="M8 0a7.992 7.992 0 0 0-6.583 12.535 1 1 0 0 0 .12.183l.12.146c.112.145.227.285.326.4l5.245 6.374a1 1 0 0 0 1.545-.003l5.092-6.205c.206-.222.4-.455.578-.7l.127-.155a.934.934 0 0 0 .122-.192A8.001 8.001 0 0 0 8 0Zm0 11a3 3 0 1 1 0-6 3 3 0 0 1 0 6Z"/>
                </svg>
                <p class="text-[#20b3fa] text-sm my-auto leading-snug ml-1">
                  Cairo
                </p>
              </span>
            </span>
          </div>
        </div>          
      </slide>
    </carousel>
  </div>
</template>

<script setup>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel'
import { reactive } from 'vue'
import { ref } from 'vue'

const props = defineProps({
  images: {
    default() {
      return []
    },
    type: Array
  },
  seats: {
    default: false,
    type: Boolean
  },
  title: {
    default: '',
    type: String
  }
})



const myCarousel = ref(null)

const settings =
  reactive[
    {
      snapAlign: 'center'
    }
  ]

const moveSLider = (action) => {
  switch(action) {
    case 'next': 
      myCarousel.value.next()
      break
    case 'prev': 
      myCarousel.value.prev()
      break

  }
}
</script>
<style>
.image_rounded-top {
  border-radius: 15px 15px 0 0;
}
</style>
