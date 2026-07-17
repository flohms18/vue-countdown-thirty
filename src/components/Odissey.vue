<script setup>

import { ref } from 'vue'

const start = ref('Alice')

let BirthdayDate = new Date("Jul 18, 2027 15:36:00").getTime();

let x = setInterval(function(){
    let NowDate = new Date().getTime();

    let gap = BirthdayDate - NowDate;

    var days = Math.floor(gap / (1000 * 60 * 60 * 24));
    var hours = Math.floor((gap % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((gap % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((gap % (1000 * 60)) / 1000);

    document.getElementById("demo").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";


})
</script>

<template>

    <div class ="Section_Title">
        <h1 class="My_Title">{{ start }}</h1>
        <h1 id="demo"></h1>
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
    font-size: 18px;
    width: 50%;
    text-align: center;

}
</style>