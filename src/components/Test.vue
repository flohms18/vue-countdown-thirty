<script setup>

let countodwnDate = new Date("1997-07-18");

let x = setInterval(function(){
    let now = new Date().getTime();
    let distance = countodwnDate - now;

    let days = Math.floor(distance / (1000 * 60 * 60 * 24));
    let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    let seconds = Math.floor((distance % (1000 * 60)) / 1000);

    
})


</script>

<template>
    
</template>