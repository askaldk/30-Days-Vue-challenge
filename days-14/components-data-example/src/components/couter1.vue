<template>
<div>
     <button class="component-button" @click="counter.count++" v-for="counter in counters" :key="counter.id">
      You clicked me {{counter.count}} times
      </button>
</div>
</template>
<script>
export default {
    data()
    {
        return{
           counters:[
               {
                   id:1,
                   count:0
               },
               {
                   id:2,
                   count:0    
               },
               {
                   id:3,
                   count:0
               }
           ]
        }
    },

    
}
</script>

