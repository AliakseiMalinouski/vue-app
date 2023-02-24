<template>
    <h3>Cписок постов</h3>
    <post-item v-for="post in posts" :post="post" v-bind:key="post.id"></post-item>
</template>

<script>
import PostItem from './PostItem.vue';
    export default {
        name: "PostList",
        components: {
            PostItem
        },
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