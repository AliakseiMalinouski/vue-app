<template>
    <button>
        <slot>
        </slot>
    </button>
</template>


<script>
    export default {
        name: "MyButton"
    }
</script>

<style>
    button {
        background-color: teal;
        color: white;
    }
</style>