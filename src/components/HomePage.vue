<template>
  <div class="relative">
    <MainCarousel />

    <EventSelection />

    <SubCarousal :images="hotelsImages" title="HOTELS" />

    <SubCarousal :images="venuesImages" title="WEDDING VENUES" :seats="true"/>

    <SubCarousal :images="plannersImages" title="WEDDING PLANNERS" />

    <SubCarousal :images="eventImages" title="EVENT PLANNERS" />

    <SubCarousal :images="EntertainersImages" title="ENTERTAINERS AND ENTERTAINMENTS" />

    <SubCarousal :images="makeUpImages" title="MAKE-UP ARTISTS" />

    <SubCarousal :images="musiciansImages" title="MUSICIANS, BANDS AND DJ'S" />
  </div>
</template>

<script setup>
import MainCarousel from '@/components/MainCarousel.vue'
import EventSelection from '@/components/EventSelection.vue'
import SubCarousal from '@/components/SubCarousal.vue'
import { reactive } from 'vue'

const hotelsImages = reactive([
  'https://eventguiders.com/wp-content/uploads/2023/02/220g0u000000jcbn1FCAF_R_960_660_R5_D.webp',
  'https://eventguiders.com/wp-content/uploads/2023/02/334002934.jpeg',
  'https://eventguiders.com/wp-content/uploads/2023/02/09997c9f9b061055847c2b5bb0719f36.jpeg',
  'https://eventguiders.com/wp-content/uploads/2023/02/exterior.jpeg',
  'https://eventguiders.com/wp-content/uploads/2023/02/220g0u000000jcbn1FCAF_R_960_660_R5_D.webp',
  'https://eventguiders.com/wp-content/uploads/2023/02/334002934.jpeg',
  'https://eventguiders.com/wp-content/uploads/2023/02/09997c9f9b061055847c2b5bb0719f36.jpeg',
  'https://eventguiders.com/wp-content/uploads/2023/02/exterior.jpeg'
])

const venuesImages = reactive([
  'https://eventguiders.com/wp-content/uploads/2022/11/istockphoto-1358757502-612x612-1.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/istockphoto-1330276716-612x612-1.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/istockphoto-1177485677-612x612-1.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/11/istockphoto-1358757502-612x612-1.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/istockphoto-1330276716-612x612-1.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/istockphoto-1177485677-612x612-1.jpeg',
  //'https://eventguiders.com/wp-content/uploads/2022/12/ES-15.-370x370-1.jpg'
])

const plannersImages = reactive([
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg',
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg'
])

const eventImages = reactive([
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg',
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg'
])

const EntertainersImages = reactive([
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg',
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg'
])

const makeUpImages = reactive([
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg',
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg'
])

const musiciansImages = reactive([
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg',
  'https://eventguiders.com/wp-content/uploads/2022/12/793535_5-reasons-a-yacht-club-wedding-venue-is.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/12/p4.jpeg',
  'https://eventguiders.com/wp-content/uploads/2022/10/Group-18248.jpg'
])
</script>


