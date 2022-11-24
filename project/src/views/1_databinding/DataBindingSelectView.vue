<template>
    <div>
        <select name="" id="" v-model="selectedCity">
            <option value=""></option>
            <option value="01">tokyo</option>
            <option value="02">osaka</option>
            <option value="03">nagoya</option>
        </select>
    </div>
</template>
<script>

export default {
    components: {},
    data () {
        return {
            selectedCity: '03'
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {}
}
</script>
