<template>
    <div>
        <input type="checkbox" name="" id="html" value="HTML" v-model="favoriteLang" />
        <label for="html">HTML</label>
    </div>
    <div>
        <input type="checkbox" name="" id="css" value="CSS" v-model="favoriteLang" />
        <label for="css">CSS</label>
    </div>
    <div>
        <input type="checkbox" name="" id="js" value="JS" v-model="favoriteLang" />
        <label for="js">JavaScript</label>
    </div>
    <div>selected Language: {{ favoriteLang }}</div>
</template>
<!--Data Two Way Binding with Attribute "checked"-->
<!--Array Data-->
<script>
export default {
    components: {},
    data () {
        return {
            favoriteLang: ['JS']
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {}
}
</script>
