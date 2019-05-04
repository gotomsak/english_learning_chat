<template>
    <div class="talk_container">
        <div class="talk_image">
            <img src="../assets/fear.png" alt="画像">
        </div>
        <div class="talk_inner1">
            <div class="talk_inner2">
                未来が見えない
            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name: "ChatLineFear"
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

    .talk_inner1 {
        padding: 10px;
        margin: 20px;

        max-width: -webkit-calc(100% - 80px);
        max-width: calc(100% - 80px);
        clear: both;
        background: #ff77ff;
        position: relative;
        float: left;
    }

    .talk_inner1::before {
        content: "";
        height: 14px;
        position: absolute;
        left: 0;
        right: 0;
        top: -14px;
        background: radial-gradient(30px circle at bottom, #ff77ff 25%, transparent 25%);
        background-size: 14px 14px;
    }

    .talk_inner1::after {
        content: "";
        height: 14px;
        position: absolute;
        left: 0;
        right: 0;
        bottom: -14px;
        background: radial-gradient(30px circle at top, #ff77ff 25%, transparent 25%);
        background-size: 14px 14px;

    }

    .talk_inner2 {
        position: relative;
        margin: 0;
    }

    .talk_inner2::before {
        content: "";
        position: absolute;
        width: 14px;
        top: -10px;
        bottom: -10px;
        left: -24px;
        background: radial-gradient(30px circle at right, #ff77ff 25%, transparent 0%);
        background-size: 14px 14px;
    }

    .talk_inner2::after {
        content: "";
        position: absolute;
        width: 14px;
        top: -10px;
        bottom: -10px;
        right: -24px;
        background: radial-gradient(30px circle at left, #ff77ff 25%, transparent 0%);
        background-size: 14px 14px;
    }



</style>