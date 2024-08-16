<template>
    <div>
        <h2>Home</h2>
        <p>hi this is Home</p>
    </div>
</template>

<script setup>
const arr = useState('array', () => [1,2,3])
console.log('arr',arr.value.filter((val)=> val%2===1));
</script>

<style scoped>

</style>