<template>
    <div>
        <h2>Home</h2>
        <p>hi this is Home</p>
    </div>
</template>

<script setup>
// const arr = useState('array', () => [])
// console.log('arr',arr.value.filter((val)=> val%2===1));
const items = useState('items');
console.log('items', items.value);
</script>

<style scoped>

</style>