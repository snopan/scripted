<template>
    <div id="text-section">
        <div id="title">{{title}}</div>
        <div id="text">{{text}}</div>
    </div>
</template>

<script>
    export default {
        name: "text-section",
        props: {
            title: String,
            text: String
        }
    }
</script>

<style scoped>
    #text-section {
        width: 100%;
        height: 100%;
    }

    #title {
        width: 100%;
        font-size: 60px;
        font-weight: bold;
    }

    #text {
        height: calc(100% - 60px - 50px);
        overflow-y: auto;
        margin-top: 50px;
        background-color: rgba(0, 0, 0, 0.4);
    }
</style>
