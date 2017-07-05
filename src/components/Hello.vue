<template>
    <div class="hello">
        <cInput class="m-i" placeholder="姓名" :value="msg"></cInput>
        <cInput class="m-i" inputType="number" placeholder="年龄" :value="msg1"></cInput>
    </div>
</template>

<script>
    import cInput from '../components/c-input'

    export default {
        name: 'hello',
        data () {
            return {
                msg: 'hellos',
                msg1: 123,
            }
        },
        methods: {},
        components: {cInput}
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