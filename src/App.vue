<script setup>
import {ref} from 'vue'
import Star from './Star.vue'

const stars = ref([1, 2, 3, 4, 5])
const selectedStar = ref(0)
const rating = ref(0)

function setRating(star) {
  rating.value = star
}

function setHoverRating(star) {
  selectedStar.value = star
}
</script>

<template>
  <span v-for="star in stars">
    <Star
      :id="star"
      :selected-star="selectedStar || rating"
      @click="setRating(star)"
      @mouseenter="setHoverRating(star)"
      @mouseleave="setHoverRating(0)"
    ></Star>
  </span>
</template>
