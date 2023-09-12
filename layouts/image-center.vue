<!-- 
Usage:
```md
---
layout: image-center
image: URL or path to image in public folder
hideBubbles: false or true
---

# Text appears above the image
```
---
 -->
<script setup lang="ts">

const props = defineProps({
  image: {
    type: String,
    required: false,
  },
  hideBubbles: {
    type: Boolean,
    default: false,
  }
});
</script>
<template>
  <div class="relative h-full w-full intro grid grid-cols-12">
    <div class="absolute h-full w-full" style="z-index: -10">
      <BubbleFrame v-if="!hideBubbles" />
    </div>
    <div class="slidev-layout col-span-12 m-auto">
      <div class="text-center">
        <slot />
      </div>
      <div v-if="image" class="m-auto w-8/12 rounded-lg manual-shadow">
        <img :src="image" class="rounded-lg" />
      </div>
    </div>
  </div>
</template>
