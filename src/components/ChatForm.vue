<template>
    <!--<div class="chat-form">-->
    <footer class="chat-form">
        <div class="form-container" v-on:keypress.enter="">
            <textarea class="message" name="message" v-model="message"></textarea>
            <!--<input type="submit" value="送信">-->
            <button class="submit" @click="submit">送信</button>
        </div>
    </footer>
    <!--</div>-->
</template>

<script>
    export default {
        name: "ChatForm",

        data() {
            return {
                message: "",
                // style: {
                //     'position': 'fixed',
                //     'height': '100px',
                //     'display': 'flex',
                //     'display': '-webkit-flex',
                //     'width': '100 %',
                //     'bottom': '0',
                //
                // },
                count: 1,
                sum_height: '500px'

            }
        },
        methods: {
            viewSize: function () {
                this.count += 1;
                console.log(this.count);
                this.sum_height = this.count * 40 + "px";
                console.log(this.sum_height);
                return {

                    style: {
                        'position': 'fixed',
                        'height': '100px',
                        'display': 'flex',
                        'display': '-webkit-flex',
                        'width': '100 %',
                        'bottom': '0',
                    }
                }
            },
            submit: function () {
                this.$emit('submit-event', this.message);
                this.message = ''
            }
        },
        // components:{
        //     'sent': Sent
        // }
        // computed: {
        //     // バインドするスタイルを生成
        //     styles() {
        //         return {
        //             '--height': this.sum_height,
        //         }
        //     }
        // }
    }
</script>


<style scoped>
    .chat-form {
        /*padding-bottom: 15%;*/
        max-height: calc(100% - 60px);

        /*box-sizing: border-box;*/
    }

    button {
        background-color: transparent;
        border: none;
        cursor: pointer;
        outline: none;
        padding: 0;
        /*appearance: none;*/
    }

    textarea {
        resize: none;
        width: 100%;
    }


    .form-container {
        box-sizing: border-box;
        --height: 40px;
        position: fixed;
        height: var(--height);
        display: flex;
        display: -webkit-flex;
        /*z-index: 1;*/
        /*padding-bottom: 10px;*/
        width: 100%;
        bottom: 0;

    }

    .message {
        position: relative;
        top: 0;
        bottom: 0;
        left: 0;
        /*right: 80px;*/
        /*width: 100%;*/
        height: 100%;
        font-size: 1.3rem;
        /*padding: 0 20px;*/

    }

    .submit {
        position: relative;
        bottom: 0;
        top: 0;
        /*right: 0;*/
        width: 80px;
        text-align: center;
        background-color: #4F83E1;
        color: white;
        font-size: 1.6rem;
    }

</style>
