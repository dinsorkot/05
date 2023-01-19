<script setup>
import G_like from './G_like.vue';

</script>

<template>
    <div class="card col-3 m-3 p-2 pic" style="max-height: 480px; overflow:scroll;" v-for="n in 6" :key="n">
        {{ n }}
        <img :src="`../src/assets/img/pic${n}.jpg`" :alt="`pic${n}`" >
        <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
                content.</p>
            <G_like />
        </div>
    </div>
</template>
<style scoped>
.pic::-webkit-scrollbar {
    display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
.pic {
  -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;  /* Firefox */
}
</style>