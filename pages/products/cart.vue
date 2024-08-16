<template>
    <div>
        <div class="flex justify-center">
            <h1 class="text-xl mb-4">Cart</h1>
        </div>
        <div class="grid grid-cols-4 gap-5">
        <div v-for="p in items">
            <ProductCard :product="p" />
        </div>
    </div>
    </div>
</template>

<script setup>
  const items = useState('items');

  definePageMeta({
    layout: "products",
  })
</script>

<style scoped>

</style>