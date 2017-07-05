<template>
    <div class="hello">
        <MInput class="m-i" mode="text" placeholder="姓名" :value="msg"></MInput>
        <MInput class="m-i" mode="number" placeholder="年龄" :value="msg1"></MInput>
    </div>
</template>

<script>
    import MInput from '../components/MInput'

    export default {
        name: 'hello',
        data () {
            return {
                msg: 'hellos',
                msg1: 123,
            }
        },
        methods: {},
        components: {MInput}
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .m-i {
        height: 48px !important;
        line-height: 48px;
        border: 1px solid #ddd;
        margin-bottom: 10px;
    }
</style>

<style>
    .m-i input {
        text-indent: 2em;
    }
</style>