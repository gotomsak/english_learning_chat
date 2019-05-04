<template>
    <div class="talk_container">
        <div class="talk_image">
            <img src="../assets/joy.png" alt="画像">
        </div>
        <div class="talk_inner">
            それは草wwwww
        </div>
    </div>
</template>

<script>
    export default {
        name: "ChatLineJoy"
    }
</script>

<style scoped>
    .talk_container {
        max-width: 500px;
        margin: 10px 20px;
        padding: 10px;
        display: -webkit-flex;
        display: flex;
        -webkit-align-items: center;
        align-items: center;
    }

    .talk_image {
        float: left;
        margin-right: 20px;
        display: -webkit-flex;
        display: flex;
        width: 30%;

    }

    .talk_inner {
        position: relative;
        background: #fff748;
        padding: 20px;
        margin: 0 10px;

        /*display: inline-block;*/
        display: -webkit-flex;
        display: flex;
        border-radius: 40%;
        max-width: -webkit-calc(100% - 80px);
        max-width: calc(100% - 80px);
        word-wrap: break-word;
    }

    .talk_inner:before {
        content: "";
        position: absolute;
        top: 50%;
        left: -30px;
        margin-top: -15px;
        border: 15px solid transparent;
        border-right: 15px solid #fff748;
    }

</style>