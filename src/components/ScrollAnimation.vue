<template>
  <div
    ref="animatedElement"
    :class="{ visible: isVisible }"
    class="animate-on-scroll"
  >
    <slot />
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const animatedElement = ref(null);
const isVisible = ref(false);

onMounted(() => {
  const observer = new IntersectionObserver(([entry]) => {
    isVisible.value = entry.isIntersecting;
  }, { threshold: 0.3 });

  if (animatedElement.value) observer.observe(animatedElement.value);
});
</script>