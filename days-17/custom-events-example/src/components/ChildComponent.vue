<template>
<div>
    <h2>{{numbers}}</h2>
    <input type="number" v-model="number">
    <button @click="$emit('NumberAdded',Number(number))">
        Add new number
    </button>
</div>
    
</template>
<script>
export default {
    name:'ChildComponent',
    props:{
        numbers:Array
    },
    data(){
        return{
            number:0
        }
    }
}
</script>
