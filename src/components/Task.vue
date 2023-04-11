<template>
    <div class="task container">
        <h2>{{ task }}</h2>
        <button @click="showBox">Show</button>
        <div class="span" v-if="show"></div>
    </div>
</template>

<script>
export default {
    name: "Task",
    props: {
        task: String,
    },
    data() {
        return {
            show: true
        }
    },
    methods: {
        showBox() {
            this.show = !this.show
        }
    }
}
</script>

<style scoped>
.task {
    width: 500px;
    height: 400px;
    background-color: #444;
    color: white;
}
.span {
    widows: 100px;
    height: 50px;
    background-color: orange;
    margin-top: 50px;
}
</style>