<template>
    <div class="card">
      <div class="grid grid-cols-2 gap-10">
        <div class="p-7">
          <img :src="`${product.image}`" class="mx-auto my-7" />
        </div>
        <div class="p-7">
          <h2 class="text-4xl my-7">{{ product.title }}</h2>
          <p class="text-xl my-7">Price - ${{ product.price }}</p>
          <h3 class="font-bold border-b-2 mb-4 pb-2">Product description:</h3>
          <p class="mb-7">{{ product.description }}</p>

          <button 
            :disabled="disable"
            class="btn flex"
            :class="{
              'cursor-not-allowed bg-[#b7e8db] text-white px-3 py-2 rounded-md text-sm text-white inline-block;': disable
            }"
            @click="addItem">
            <i class="material-icons mr-2">add_shopping_cart</i>
            <span>Add to cart</span>
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
    const { product } = defineProps(['product'])
   // Define state with an array
    const items = useState('items', () => []);
    const disable = ref(false);
    // Function to add an item
    const addItem = () => {
        disable.value = true;
        items.value.push(product);
        console.log(items.value);
        alert("item added")
    };
   
  </script>
  
  <style scoped>
    img {
      max-width: 400px;
    }
  </style>