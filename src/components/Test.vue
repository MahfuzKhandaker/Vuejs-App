<template>
    <div class="test">
        <input type="text" v-model="msg"><br>
        <p>{{msg}}</p>
        <button v-on:click="rvMsg">Reverse Message</button>
    <ul>
       <li v-for=" item in groceryList" :key="item.text">{{item.text}}</li>
    </ul>
    <br>
    <label> First Name </label> <input type="text" v-model="user.f_name">
    <br>
    <label> Last Name </label> <input type="text" v-model="user.l_name">
    <h3>{{ fullName }}</h3>
    <h2>{{ msg }}</h2>
    </div>
</template>

<script>
export default {
    name: 'Test',
    props: {
        type: String,
    },
    data() {
        return{
            msg:'Hello Developer',
            user: { 
                f_name: 'Mahfuz',
                l_name: 'Khandaker'
                },
            groceryList: [
                { text: 'Vegetables'},
                { text: 'Milk'},
                { text: 'Fish'},
                { text: 'Meat'},
                { text: 'Fruits'}
            ]
    }
    },
    methods:{
        rvMsg: function(){
            this.msg = this.msg.split('').reverse().join('')
        }
        },
        computed: {
            fullName: function(){
                return this.user.f_name+ ' ' +this.user.l_name
            }

        }
   }
</script>

<style scoped>

</style>

