<script setup>
import ICunlike from './icons/dislike.vue';
import IClike from './icons/like.vue';
import { ref } from 'vue';
const like = ref(0);
const dislike = ref(0);
function likeS() {
    like.value++;
}
function Sads() {
    dislike.value++;
}
</script>

<template>
    <div class="d-flex flex-row">
        <div name="like">
            <button class="btn btn-primary m-1" @click="likeS()">
                <IClike />
                {{ like }}
            </button>
        </div>
        <div name="dislike">
            <button class="btn btn-danger m-1" @click="Sads()">
                <ICunlike />
                {{ dislike }}
            </button>
        </div>
    </div>
</template>