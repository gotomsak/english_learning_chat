<template>
    <div class="talk_container">
        <div class="talk_image">
            <img src="../assets/sadness.png" alt="画像">
        </div>
        <div class="none_content">
            <div class="emphasis_left">((</div>
            <div class="talk_inner1">
                <div class="talk_inner2">
                    だん長おおおおおおお
                </div>
            </div>
            <div class="emphasis_right">))</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ChatLineSadness"
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

        clear: both;
        background: #5ff7ff;
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
        background: radial-gradient(30px circle at bottom, #5ff7ff 25%, transparent 25%);
        background-size: 14px 14px;
    }

    .talk_inner1::after {
        content: "";
        height: 14px;
        position: absolute;
        left: 0;
        right: 0;
        bottom: -14px;
        background: radial-gradient(30px circle at top, #5ff7ff 25%, transparent 25%);
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
        background: radial-gradient(30px circle at right, #5ff7ff 25%, transparent 0%);
        background-size: 14px 14px;
    }

    .talk_inner2::after {
        content: "";
        position: absolute;
        width: 14px;
        top: -10px;
        bottom: -10px;
        right: -24px;
        background: radial-gradient(30px circle at left, #5ff7ff 25%, transparent 0%);
        background-size: 14px 14px;
    }

    .emphasis_left {
        margin: 0;
        position: absolute;
        transform: rotate(30deg);
        -moz-transform: rotate(30deg);
        -webkit-transform: rotate(30deg);
    }

    .emphasis_right {
        margin: 0;
        position: absolute;
        transform: rotate(30deg);
        -webkit-transform: rotate(30deg);
        bottom: 0;
        right: 0px;

    }

    .none_content {
        position: relative;
        margin: 0;
        display: -webkit-flex;
        display: flex;
        max-width: -webkit-calc(100% - 80px);
        max-width: calc(100% - 80px);
    }


</style>