<template>
    <div>
        <form @submit.prevent>
        <h4>Создание поста</h4>
        <input v-model="post.title"   type="text" placeholder="Название"/>
        <input v-model="post.body"   type="text" placeholder="Описание"/>
        <my-button @click="createPost">Создать</my-button>
        </form>
  </div>
</template>


<script>

import MyButton from './UI/MyButton.vue';

export default {
    name: "PostForm",
    components: {
        MyButton
    },
    data () {
        return {
            post: {
                title: "",
                body: ""
            }
        }
    },
    methods: {
        createPost () {
            this.post.id = Date.now();
            this.$emit('create', this.post);
            this.post = {
                title: "",
                body: ""
            }
        }
    }
}

</script>


<style>

form {
  padding-bottom: 50px;
}

input {
  width: 300px;
  height: 35px;
  padding: 10px 15px;
  margin-right: 15px;
}

</style>