<template>
  <div class="app">
    <p class="p">Oke lah </p>
    <button class="bttn" @click="ubahTeks">Submit</button>
    <button class="cncl" @click="batalTeks">Cancel</button>
  </div>
</template>

<script setup>
const emit = defineEmits(['response', 'cancel'])

function ubahTeks() {
  emit('response', 'shuuuu')
}

function batalTeks() {
  emit('cancel', 'shuiiiii')
}
</script>

<style scoped>
button {
  margin: 0 20px;
}

.bttn {
  background-color: green;
}

.cncl {
  background-color: red;
}

.p{
  color: white;
}
</style>
