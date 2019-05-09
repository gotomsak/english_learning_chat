<template>


    <div class="talk_container">

        <div class="talk_inner">{{message}}</div>

    </div>

</template>

<script>
    import ChatForm from'./ChatForm'
    export default {
        components:{
            ChatForm
        },
        name: "Sent",
        data(){
            return {

            }

        },
        props:[
            'message'
        ],
        // methods: {
        //     check :function (value) {
        //         console.log(value);
        //         this.message=value
        //         console.log(this.message)
        //     }
        // }
    }
</script>

<style scoped>
    /*.talk_none{*/
        /**/
    /*}*/
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
        /*float: right;*/
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