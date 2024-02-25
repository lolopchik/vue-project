<script>
export default {
    props: {

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
            <p class="card-subtitle text-secondary">Автор поста</p>
            <h3 class="card-title">Заголовок поста</h3>
            <p class="card-text">Текст поста</p>
            <div class="d-flex justify-content-between align-items-center ">
                <div class="btn-group">
                    <div class="btn-group">
                        <button type="button" class="btn btn-sm btn-outline-secondary">-</button>
                        <button type="button" class="btn btn-sm btn-outline-secondary">+</button>
                    </div>
                    <!-- <input v-model="fontSizeNew" class="form-control ms-3" type="text" placeholder="px" style="width: 50px;">
                    <button type="button" class="btn btn-sm btn-outline-secondary">Установить</button> -->

                </div>
                <small class="text-body-secondary">Дата поста</small>
            </div>

            <hr>
            <h4>Комментарии:</h4>
            <ul class="list-group list-group-flush">
                <!-- Вывод всех комментарии -->
                <li class="list-group-item" >Аноним: Я аноним</li>
            </ul>

        </div>
    </div>
</template>
<style>
</style>