<template>
    <div>
        <select name="" id="">
            <option value=""></option>
            <option :value="city.code" :key="city.code" v-for="city in cities">
                {{ city.title }}
            </option>
        </select>
    </div>
    <div>
        <table>
            <thead>
                <tr>
                    <th>Id</th>
                    <th>Name</th>
                    <th>Price</th>
                    <th>Quantity</th>
                    <th>Total</th>
                </tr>
            </thead>
            <tbody>
                <tr :key="drink.drinkId" v-for = "drink in drinkList">
                    <td> {{ drink.drinkId }}</td>
                    <td> {{ drink.drinkName }}</td>
                    <td> {{ drink.price }}</td>
                    <td><input type="number" name="" id="" v-model="drink.qty"></td>
                    <td>{{ drink.price * drink.qty }}</td>
                </tr>
            </tbody>
        </table>
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
            ],
            drinkList: [
                {
                    drinkId: '1',
                    drinkName: 'Cola',
                    price: 700,
                    qty: 1
                },
                {
                    drinkId: '2',
                    drinkName: 'Cidar',
                    price: 700,
                    qty: 1
                },
                {
                    drinkId: '3',
                    drinkName: 'Lemonade',
                    price: 800,
                    qty: 1
                },
                {
                    drinkId: '4',
                    drinkName: 'MelonSoda',
                    price: 600,
                    qty: 1
                },
                {
                    drinkId: '5',
                    drinkName: 'GingerAle',
                    price: 850,
                    qty: 1
                }
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
