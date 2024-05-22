<template>
    <div class="app2">
        <h1 class="p">Yahayuk</h1>
        <p class="p">
            Perkenalkan Nama saya Dany, saya kuliah di Universitas Islam Riau.
        </p>
        <Title title="Emit" />
        <p :class="{ 'p': childMsg !== 'Tidak ada pesan' }">{{ childMsg }}</p>
        <Button @response="ubahTeks" @cancel="ubahb" />
        <SoltCom/>
    </div>
</template>

<script setup>
import Button from './components/button.vue'
import { ref } from 'vue'
import SoltCom from './components/solt.vue'

const childMsg = ref('Tidak ada pesan')

function ubahTeks(msg) {
childMsg.value = msg
alert('Pesan yang diterima dari child : ' + msg)
}

function ubahb(msg) {
    childMsg.value = msg
    alert('Pesan yang diterima dari child: ' + msg)
}
</script>

<style scoped>
.app2 {
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
    border: 2px solid rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.p {
    color: white;
}


</style>
