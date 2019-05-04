<template>
    <div class="talk_container">
        <div class="talk_image">
            <img src="../assets/anger.png" alt="画像">
        </div>
        <!--<div class="talk_inner">-->
            <!--燃え上がれ燃え上がれ燃え上がれガンダム-->
        <!--</div>-->
        <div class="talk_inner1">
            <div class="talk_inner2">激おこぷんぷん丸だよー</div>
        </div>
    </div>

</template>

<script>
    export default {
        name: "ChatLineAnger"
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
        background: #ff2d16;
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
        background: linear-gradient(45deg, #ff2d16 25%, transparent 0%), linear-gradient(315deg, #ff2d16 25%, transparent 0%), linear-gradient(-225deg, transparent 25%, transparent 0%) -7px 0, linear-gradient(135deg, transparent 25%, transparent 0%) -7px 0;
        background-size: 14px 14px;
    }

    .talk_inner1::after {
        content: "";
        height: 14px;
        position: absolute;
        left: 0;
        right: 0;
        bottom: -14px;
        background: linear-gradient(135deg, #ff2d16 25%, transparent 25%), linear-gradient(225deg, #ff2d16 25%, transparent 25%), linear-gradient(315deg, transparent 25%, transparent 25%) -7px 0, linear-gradient(45deg, transparent 25%, transparent 25%) -7px 0;
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
        background: linear-gradient(45deg, transparent 25%, transparent 0%), linear-gradient(315deg, #ff2d16 25%, transparent 0%), linear-gradient(-225deg, transparent 25%, transparent 0%), linear-gradient(-135deg, #ff2d16 25%, transparent 0%);
        background-size: 14px 14px;
    }

    .talk_inner2::after {
        content: "";
        position: absolute;
        width: 14px;
        top: -10px;
        bottom: -10px;
        right: -24px;
        background: linear-gradient(45deg, #ff2d16 25%, transparent 0%), linear-gradient(315deg, transparent 25%, transparent 0%), linear-gradient(-225deg, #ff2d16 25%, transparent 0%), linear-gradient(-135deg, transparent 25%, transparent 0%);
        background-size: 14px 14px;
    }


</style>