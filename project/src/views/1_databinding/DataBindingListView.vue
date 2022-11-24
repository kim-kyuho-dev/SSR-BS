<template>
    <div>
        <select name="" id="">
            <option value=""></option>
            <option :value="city.code" :key="city.code" v-for="city in cities">
                {{ city.title }}
            </option>
        </select>
    </div>
</template>
<script>

export default {
    components: {},
    data () {
        return {
            cities: [
                { title: 'tokyo', code: '01' },
                { title: 'osaka', code: '02' },
                { title: 'nagoya', code: '03' }
            ]
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {}
}
</script>
