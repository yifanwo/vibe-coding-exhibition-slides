<script setup>
import { onMounted, onUnmounted } from 'vue'
import { useNav } from '@slidev/client'

const { next, prev } = useNav()

let locked = false

function handleWheel(event) {
  if (locked)
    return

  if (Math.abs(event.deltaY) < 20)
    return

  locked = true

  if (event.deltaY > 0)
    next()
  else
    prev()

  setTimeout(() => {
    locked = false
  }, 500)
}

onMounted(() => {
  window.addEventListener('wheel', handleWheel)
})

onUnmounted(() => {
  window.removeEventListener('wheel', handleWheel)
})
</script>

<template></template>