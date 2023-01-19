<script setup>
import G_like from './G_like.vue';
</script>
<script>
export default {
    data() {
        return {
            cards: [
                {
                    image: 'src/assets/img/pic1.jpg',
                    alt: 'pic1',
                    title: 'Card title 1',
                    content: 'Card content 1'
                },
                {
                    image: 'src/assets/img/pic2.jpg',
                    alt: 'pic2',
                    title: 'Card title 2',
                    content: 'Card content 2'
                },
                {
                    image: 'src/assets/img/pic3.jpg',
                    alt: 'pic3',
                    title: 'Card title 3',
                    content: 'Card content 3'
                },
                {
                    image: 'src/assets/img/pic4.jpg',
                    alt: 'pic4',
                    title: 'Card title 4',
                    content: 'Card content 4'
                },
                {
                    image: 'src/assets/img/pic5.jpg',
                    alt: 'pic5',
                    title: 'Card title 5',
                    content: 'Card content 5'
                },
                {
                    image: 'src/assets/img/pic6.jpg',
                    alt: 'pic6',
                    title: 'Card title 6',
                    content: 'Card content 6'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="card col-3 m-3 p-2 pic" style="max-height: 480px; overflow:scroll;" v-for="(pic , n) in cards" :key="n">
        {{ n+1 }}
        <img :src="pic.image" :alt="pic.alt">
        <div class="card-body">
            <h5 class="card-title">{{ pic.title }}</h5>
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
    -ms-overflow-style: none;
    /* IE and Edge */
    scrollbar-width: none;
    /* Firefox */
}
</style>