<template>
    <div class="m-input">
        <div class="m-clear-input" v-show="inputValue.toString().length" @click="funClearIcon"></div>
        <input type="text" :value="inputValue" v-model="inputValue" :placeholder="thisPlaceholder" v-if="inputType=='text'">
        <input type="number" :value="inputValue" v-model="inputValue" :placeholder="thisPlaceholder" v-if="inputType=='number'">
    </div>
</template>

<script>
    export default {
        name: 'mInput',
        props: {
            inputType: {
                type: String,
                default: 'text'
            },
            value: {
                default: '...'
            },
            placeholder: {
                type: String
            }
        },
        data () {
            return {
                type: this.mode,
                inputValue: this.value,
                thisPlaceholder: this.placeholder
            }
        },
        methods: {
            funClearIcon () {
                this.inputValue = ''
            }
        }
    }
</script>

<style scoped>
    * {
        margin: 0;
        padding: 0;
    }

    .m-input {
        position: relative;
        height: 50px;
    }

    .m-input input {
        width: 100%;
        height: 100%;
        border: none;
        font-size: 18px;
        outline: none;
    }

    .m-input .m-clear-input {
        position: absolute;
        top: 50%;
        right: 10px;
        width: 32px;
        height: 32px;
        transform: translateY(-50%);
        background-size: 100% 100%;
        background-image: url("../assets/images/clear.png");
        text-align: center;
    }
</style>