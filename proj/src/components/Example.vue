<template>
<div class="hello">
    <h1> HARINATH REDDY SADARA</h1>
    <h1>sddhjgdsjghjd</h1>
    <p>{{ fun() }}</p>
    <button @click='count++'> Increase</button>
    <button @click='count--'> Decrease</button>
    <a href="https://google.com">GOOGLE</a>
    <a :href="link"> FACEBOOK</a>
    <p> {{count}}</p>
    <table border="1px">
        <tr>
        <th>NAME</th>
        <th>ROLL</th>
        <th>DEP</th>
        </tr>
        <tr  v-for="item in person">
            <td>{{item.name}}</td>
            <td>{{item.roll}}</td>
            <td>{{item.dep}}</td>
        </tr>
    </table>
    <input type='text' v-model="update">
    <p>{{ update }}</p>
    <P>FIRST NAME:{{firstname}}</p>
    <p>LAST NAME:{{lastname}}</p>
    <p> DETAILS:{{details()}}</p>
</div>
</template>
<script>
export default {
    data(){
        return{
        title:'HELLO....!',
        count:0,
        link:"https://facebook.com",
        update:'type here to udate',
        person:[{name:'harinath',roll:540,dep:'cse'},{name:'harikiran',roll:539,dep:'cse'},{name:'girish',roll:535,dep:'cse'}],
        firstname:'HARINATH REDDY',
        lastname:'SADARA',
        

        }
    },
    methods:{
    fun:function(){
        return this.title;
    },
    details:function(){
        return " I'm" + this.firstname +" "+ this.lastname +" "+" from HINDUPUR";
    }
    }
}
</script>
<style>
table,tr,td,th{
    border-collapse: collapse;
}
</style>
