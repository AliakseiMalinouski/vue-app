<template>
    <div class="post" v-for="post in posts" v-bind:key="post.id">
        <div><strong>Название: </strong>{{ post.title }}</div>
        <div><strong>Описание: </strong>{{ post.body }}</div>
  </div>
</template>

<script>
    export default {
        name: "PostList",
        props: {
            posts: {
                type: Array,
                required: true
            }
        }
    }

</script>

<style>
    .post {
    width: 100%;
    padding: 15px;
    border: 1px solid teal;
    }
</style>