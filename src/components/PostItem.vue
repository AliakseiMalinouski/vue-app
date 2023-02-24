<template>
    <div>
        <div class="post">
            <div><strong>Название: </strong>{{ post.title }}</div>
            <div><strong>Описание: </strong>{{ post.body }}</div>
    </div>
    <div class="delete">
        <button>Удалить</button>
    </div>
    </div>
</template>


<script>
    export default {
        props: {
            post: {
                type: Object,
                required: true
            }
        }
    }
</script>


<style scoped>
.post {
    width: 100%;
    padding: 15px;
    border: 1px solid teal;
    }
</style>