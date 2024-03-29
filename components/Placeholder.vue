<template>
  <div class="relative">
        <img class="object-cover rounded-xl" src="https://assets-global.website-files.com/643b269c094e51b9d34a4a21/6479352fa9abff97d715bdc3_demo_img.webp"/>
  </div>
</template>

<style scoped>
.border-gradient:after {
  --angle: 0deg;
  --border-color: rgb(var(--color-gray-300));
  --highlight-color: rgb(var(--color-primary-500));

  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: -1px;
  opacity: 0.5;
  border-radius: 0.8rem;
  z-index: -1;
  background: var(--border-color);

  @supports (background: paint(houdini)) {
    background: linear-gradient(var(--angle), var(--border-color), var(--border-color), var(--border-color), var(--border-color), var(--highlight-color));
    animation: 10s rotate linear infinite;
  }
}

.dark .border-gradient:after {
  --border-color: rgb(var(--color-gray-700));
  --highlight-color: rgb(var(--color-gray-400));
}

@keyframes rotate {
  to {
    --angle: 360deg;
  }
}

@property --angle {
  syntax: '<angle>';
  initial-value: 0deg;
  inherits: false;
}
</style>
