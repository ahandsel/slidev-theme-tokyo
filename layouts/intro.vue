<!--
Usage:

```md
---
layout: intro
image: URL or path to image in public folder
---

# Title

Text
```
-->
<template>
  <div class="slidev-layout intro">
    <div class="my-auto">
      <slot />
    </div>
  </div>
</template>
