<script setup>

const start = ref(new Date(Date.UTC(2027, 7, 18, 3, 3, 3)))


</script>

<template>

    <div class="Section_Title">
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
    font-size: 18px;
    width: 50%;
    text-align: center;

}
</style>