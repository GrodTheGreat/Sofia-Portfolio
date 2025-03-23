<script setup>
const images = await import.meta.glob("@/assets/images/*", { eager: true });
const imgUrls = Object.values(images).map((mod) => mod.default);
</script>

<template>
  <div class="grid">
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
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 12px;
  justify-items: center;
  align-items: center;
  width: 100%;
}

.grid img {
  /* width: 100%; */
  height: 250px;
  border-radius: 1rem;
}
</style>
