<template>
    <div>
        <!--<input type="search" name="" id="" @keyup="checkEnter($event)" v-model="searchText" />-->
        <input type="search" name="" id="" @keyup.enter="doSearch" v-model="searchText" />
        <button @click="doSearch">Search</button>
        <button type="subit" @click.prevent="doSearch"></button>
    </div>
</template>
<!--
//.enter
//.tab
//.delete
//.esc
//.space
//.up
//.down
//.right
//.left
//.stop - event.stopPropagation();
//.prevent - event.preventDefault();
-->
<script>
export default {
    components: {},
    data () {
        return {
            sampleData: ''
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {
        doSearch () {
            console.log(this.searchText)
        },
        checkEnter (event) {
            //  event.stopPropagation();
            if (event.keyCode === 13) {
                this.doSearch()
            }
        }
    }
}
</script>
