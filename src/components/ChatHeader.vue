<template>
    <div class="header">
        <div class="header_inner">
            nyan
        </div>
    </div>
</template>

<script>
    export default {
        name: "ChatHeader"
    }
</script>

<style scoped>

    .header {
        position: fixed;
        display: flex;
        top: 0;
        left: 0;
        width: 100%;
        height: 5%;
        background-color: #31a9ee;
        justify-content: center;
        z-index: 1;
    }

    .header_inner {
        position: absolute;
        top: 50%;
        left: 50%;
        -webkit-transform: translateY(-50%) translateX(-50%);
        transform: translateY(-50%) translateX(-50%);
        color: #fbfffb;
        padding: 20px;
        font-size-adjust: 1;
    }

</style>