<script setup>

import { onMounted, ref } from 'vue'

const start = ref('')

onMounted(() => {
    const BirthdayDate = new Date("Jul 18, 2027").getTime()

    setInterval(function () {
        const NowDate = new Date().getTime()
        const gap = BirthdayDate - NowDate

        const days = Math.floor(gap / (1000 * 60 * 60 * 24))
        const hours = Math.floor((gap % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))
        const minutes = Math.floor((gap % (1000 * 60 * 60)) / (1000 * 60))
        const seconds = Math.floor((gap % (1000 * 60)) / 1000)

        start.value = `${days} : ${hours} : ${minutes} : ${seconds}`
    }, 1000)
})
</script>

<template>

    <div class ="Section_Title">
        <h1 class="My_Title">{{ start }}</h1>
    </div>

</template>

<style scoped>


.Section_Title {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.My_Title {
    font-size: 42px;
    width: 50%;
    text-align: center;

}
</style>