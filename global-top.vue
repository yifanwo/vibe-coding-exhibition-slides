<script setup>
import { onMounted, onUnmounted } from 'vue'
import { useNav } from '@slidev/client'

const { next, prev } = useNav()

let locked = false

function findScrollableParent(el) {
  while (el && el !== document.body) {
    const style = getComputedStyle(el)
    const overflowY = style.overflowY

    if (
      (overflowY === 'auto' || overflowY === 'scroll') &&
      el.scrollHeight > el.clientHeight
    ) {
      return el
    }

    el = el.parentElement
  }

  return null
}

function handleWheel(event) {
  const scrollable = findScrollableParent(event.target)

  if (scrollable) {
    const atTop = scrollable.scrollTop <= 0
    const atBottom =
      scrollable.scrollTop + scrollable.clientHeight >=
      scrollable.scrollHeight - 1

    // Let the inner area scroll normally
    if (event.deltaY > 0 && !atBottom)
      return

    if (event.deltaY < 0 && !atTop)
      return
  }

  // Slide navigation
  if (locked || Math.abs(event.deltaY) < 20)
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