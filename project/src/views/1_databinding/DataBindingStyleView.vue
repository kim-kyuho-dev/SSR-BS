<template>
    <div>
        <div style="color: red; font-size: 30px">Style Binding</div>
        <div :style="style1">Style Binding</div>
        <button @click="style1.color='blue'">Change Color</button>
    </div>
</template>
<script>
export default {
    components: {},
    data () {
        return {
            style1: {
                color: 'green',
                fontSize: '30px'
            }
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {}
}
</script>
