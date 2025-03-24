<script setup>
const images = await import.meta.glob("@/assets/images/*", { eager: true });
const imgUrls = Object.values(images).map((mod) => mod.default);
</script>

<template>
  <div class="gallery">
    <img
      v-for="(url, index) in imgUrls"
      :key="index"
      :src="url"
      alt=""
      height="250"
    />
  </div>
</template>

<style scoped>
.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
  padding: 32px;
  justify-content: space-evenly;
}

.gallery img {
  display: block;
  height: 250px;
  width: auto;
  border-radius: 1rem;
  object-fit: cover;
}
</style>
