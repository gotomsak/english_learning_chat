<template>
    <div >
    <chat-line></chat-line>
        <chat-line-joy></chat-line-joy>
        <chat-line-anger></chat-line-anger>
        <chat-line-sadness></chat-line-sadness>
        <chat-line-fear></chat-line-fear>
    <sent></sent>
        </div>
</template>

<script>
    import ChatLine from '../components/ChatLine'
    import ChatHeader from '../components/ChatHeader'
    import ChatLineJoy from '../components/ChatLineJoy'
    import ChatLineAnger from '../components/ChatLineAnger'
    import ChatLineSadness from '../components/ChatLineSadness'
    import ChatLineFear from "../components/ChatLineFear";
    import Sent from "../components/Sent";
    import ChatForm from "../components/ChatForm";
    import ChatView from "../views/ChatView";
    export default {
        name: "ChatView",
        components: {
            ChatView,
            ChatForm,
            Sent,
            ChatLineFear,
            ChatLine,
            ChatHeader,
            ChatLineJoy,
            ChatLineAnger,
            ChatLineSadness
        }
    }
</script>

<style scoped>

</style>