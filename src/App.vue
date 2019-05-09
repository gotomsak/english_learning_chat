<template>
    <div id="app">
        <div class="chat-timeline">
            <chat-header></chat-header>
            <chat-line></chat-line>
            <chat-line-joy></chat-line-joy>
            <chat-line-anger></chat-line-anger>
            <chat-line-sadness></chat-line-sadness>
            <chat-line-fear></chat-line-fear>

            <sent v-for="message in messageLog" v-bind:message="message" class="talk_none"></sent>
        </div>
        <chat-form v-on:submit-event="check">
        </chat-form>
    </div>
</template>

<script>

    import ChatLine from './components/ChatLine'
    import ChatHeader from './components/ChatHeader'
    import ChatLineJoy from './components/ChatLineJoy'
    import ChatLineAnger from './components/ChatLineAnger'
    import ChatLineSadness from './components/ChatLineSadness'
    import ChatLineFear from "./components/ChatLineFear";
    import Sent from "./components/Sent";
    import ChatForm from "./components/ChatForm";

    export default {
        name: 'app',

        data() {
            return {
                message: '',
                messageLog: []
            }

        },
        components: {

            ChatForm,
            Sent,
            ChatLineFear,
            ChatLine,
            ChatHeader,
            ChatLineJoy,
            ChatLineAnger,
            ChatLineSadness
        },
        methods: {
            check: function (value) {
                if (value !== '') {
                    this.messageLog.push(value);

                    // const target = document.querySelectorAll('.chat-timeline');
                    // console.log(target)
                    setTimeout(() => {
                        this.scrollDown();
                    },100);

                }

            },
            scrollDown() {
                const target = document.querySelector('.chat-timeline');
                setTimeout(() => {
                    // const height = target.scrollHeight - target.offsetHeight;
                    scrollTo(0, target.clientHeight);
                    // if (height <= target.scrollTop) {
                    //     return;
                    // } else {
                    //     this.scrollDown();
                    // }
                }, 0);
            }

        }
    }
</script>


<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }

    .talk_none {
        padding-bottom: 15%;
        clear: both;
        /*display: block;*/
        /*flex-direction: column*/
    }

    .chat-timeline {
        overflow-y: auto;
        padding-bottom: 5%;


    }
</style>
