<script setup>
import { RouterView } from 'vue-router'
import StayTuned from '@/components/StayTuned.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <StayTuned />

      <!-- <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->
    </div>
  </header>

  <RouterView />
</template>
