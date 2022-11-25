<template>
    <div>
        <!-- @ or v on:-->
        <select name="" id="" @change="changeCity($event)" v-model="selectedCity">
            <option value="">--select city--</option>
            <option :value="city.cityCode" :key="city.cityCode" v-for="city in cityList">{{ city.title }}</option>
        </select>
        <select name="" id="">
            <option :value="ku.kuCode" :key="ku.kuCode" v-for="ku in selectedKuList">{{ ku.kuTitle }}</option>
        </select>
        <!--No Event Code-->
        <select name="" id="">
            <option :value="ku.kuCode" :key="ku.kuCode" v-for="ku in kuList.filter((ku) => ku.cityCode === this.selectedCity)">{{ ku.kuTitle }}</option>
        </select>
    </div>
</template>
<script>
export default {
    components: {},
    data () {
        return {
            selectedCity: '',
            cityList: [
                { cityCode: '01', title: 'tokyo' },
                { cityCode: '02', title: 'osaka' },
                { cityCode: '03', title: 'nagoya' }
            ],
            kuList: [
                { cityCode: '01', kuCode: '1', kuTitle: 'tokyo1' },
                { cityCode: '01', kuCode: '2', kuTitle: 'tokyo2' },
                { cityCode: '01', kuCode: '3', kuTitle: 'tokyo3' },
                { cityCode: '01', kuCode: '4', kuTitle: 'tokyo4' },
                { cityCode: '02', kuCode: '1', kuTitle: 'osaka1' },
                { cityCode: '02', kuCode: '2', kuTitle: 'osaka2' },
                { cityCode: '02', kuCode: '3', kuTitle: 'osaka3' },
                { cityCode: '03', kuCode: '1', kuTitle: 'nagoya1' },
                { cityCode: '03', kuCode: '2', kuTitle: 'nagoya2' }
            ],
            selectedKuList: []
        }
    },
    setup () {},
    created () {},
    mounted () {},
    unmounted () {},
    methods: {
        changeCity (event) {
            console.log(event.target.tagName)
            this.selectedKuList = this.kuList.filter((ku) => ku.cityCode === this.selectedCity)
        }
    }
}
</script>
