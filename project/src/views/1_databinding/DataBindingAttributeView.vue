<template>
    <div>
        <input type="text" name="" id="" v-bind:value="userId" readonly />
        <input type="text" name="" id="" :value="userId" readonly />
        <br>
        <img :src="imgSrc" alt="" style="width: 100px; height: auto;" />
        <br>
        <input type="search" name="" id="" v-model="txt1" />
        <button :disabled="txt1 === ''">search</button>
    </div>
</template>
<script>
export default {
    components: {},
    data () {
        return {
            userId: 'Test Input',
            imgSrc: 'https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Grosser_Panda.JPG/1200px-Grosser_Panda.JPG',
            txt1: ''
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {}
}
</script>
