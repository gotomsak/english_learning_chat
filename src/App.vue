<template>
    <p id="app">
        <chat-header></chat-header>
        <chat-line></chat-line>
        <chat-line-joy></chat-line-joy>
        <chat-line-anger></chat-line-anger>
        <chat-line-sadness></chat-line-sadness>
        <chat-line-fear></chat-line-fear>
        <sent></sent>
    </p>
</template>

<script>

    import ChatLine from './components/ChatLine'
    import ChatHeader from './components/ChatHeader'
    import ChatLineJoy from './components/ChatLineJoy'
    import ChatLineAnger from './components/ChatLineAnger'
    import ChatLineSadness from './components/ChatLineSadness'
    import ChatLineFear from "./components/ChatLineFear";
    import Sent from "./components/Sent";
    export default {
        name: 'app',
        components: {
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

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;

    }
</style>
