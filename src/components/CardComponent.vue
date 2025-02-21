<script setup>
const props = defineProps(['image', 'name', 'category', 'imageAlt', 'link'])
</script>

<template>
  <div class="card">
    <a :href="link">
      <div class="content">
        <img class="front-image" :src="props.image" :alt="props.imageAlt" />
        <div class="category">
          <p>
            <strong>{{ props.category }}</strong>
          </p>
        </div>
      </div>
    </a>
  </div>
</template>

<style scoped>
.card {
  width: 100%;
  height: auto;
  box-shadow: 0px 0px 10px 1px #000000ee;
  border-radius: 5px;
  overflow: hidden;
  background-color: var(--color-primary-light);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;
}

.content {
  width: 100%;
  text-align: center;
}

.front-image {
  width: 100%;
  height: auto;
  max-height: 300px;
  object-fit: cover;
  aspect-ratio: 16/9;
  object-position: center;
  padding: 0.5rem;
  border-radius: 1rem;
}

.category {
  box-shadow: 0px 0px 10px 5px #00000088;
  width: 100%;
  padding: 5px;
  background-color: var(--color-primary-base);
  color: white;
  backdrop-filter: blur(5px);
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
