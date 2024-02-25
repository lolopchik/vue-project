<script>
export default {
    props: {
        post: Object,
        fontSize: Number,
    },
    data() {
        return {

        }
    },
}
</script>
<template>
    <div class="card shadow-sm">
        <svg class="bd-placeholder-img card-img-top" width="100%" height="225" xmlns="http://www.w3.org/2000/svg" role="img"
            aria-label="Placeholder: Thumbnail" preserveAspectRatio="xMidYMid slice" focusable="false">
            <title>Placeholder</title>
            <rect width="100%" height="100%" fill="#55595c"></rect><text x="50%" y="50%" fill="#eceeef"
                dy=".3em">Thumbnail</text>
        </svg>
        <div class="card-body">
            <p class="card-subtitle text-secondary">{{post.author}}</p>
            <h3 class="card-title">{{post.title}}</h3>
            <p class="card-text" :style="{ 'font-size': fontSize + 'px' }">{{ post.text }}</p>
            <div class="d-flex justify-content-between align-items-center ">
                <div class="btn-group">
                    <div class="btn-group">
                        <button type="button" class="btn btn-sm btn-outline-secondary" @click="$emit('fontSizeDecrease')">-</button>
                        <button type="button" class="btn btn-sm btn-outline-secondary" @click="$emit('fontSizeIncrease')">+</button>
                    </div>
                    <input v-model="fontSizeNew" class="form-control ms-3" type="text" placeholder="px" style="width: 50px;">
                    <button type="button" class="btn btn-sm btn-outline-secondary" @click="$emit('fontSizeSet', fontSizeNew)">Установить</button> 

                </div>
                <small class="text-body-secondary">{{post.date}}</small>
            </div>

            <hr>
            <h4>Комментарии:</h4>
            <ul class="list-group list-group-flush" >
                <!-- Вывод всех комментарии -->
                <li class="list-group-item" v-for="comment in post.comments">Аноним: {{comment}}</li>
            </ul>
        </div>
    </div>
</template>
<style>
</style>