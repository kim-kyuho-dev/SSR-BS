<template>
    <div :class="{ 'active': isActive, 'text-red': hasError }">Class Binding</div>
    <div :class=class2>Class Binding2</div>
</template>
<script>

export default {
    components: {},
    data () {
        return {
            isActive: false,
            hasError: false,
            class2: ['active', 'text-red']
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {}
}
</script>
<style scoped>
.active {
    background-color: chartreuse;
    font-weight: bold;
}
.text-red {
    color: red;
}
</style>
