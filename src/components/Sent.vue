<template>


    <div class="talk_container">

        <div class="talk_inner">
        </div>
    </div>

</template>

<script>
    export default {
        name: "Sent"
    }
</script>

<style scoped>

    .talk_container {
        max-width: 500px;
        float: right;
        margin: 10px 20px;
        padding: 10px;
        display: -webkit-flex;
        display: flex;
        -webkit-align-items: center;
        align-items: center;
    }


    .talk_inner {
        position: relative;
        background: #51ff20;
        padding: 20px;
        margin: 0 10px;



        display: -webkit-flex;
        display: flex;
        border-radius: 10px;
        word-wrap: break-word;
    }

    .talk_inner:before {
        content: "";
        position: absolute;
        top: 50%;
        right: -30px;
        margin-top: -15px;
        border: 15px solid transparent;
        border-left: 15px solid #51ff20;
    }


</style>