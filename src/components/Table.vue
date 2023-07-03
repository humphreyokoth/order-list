<script setup lang="">
new Vue({
   el:"#app",
   data:()=>({
    items: [
        {
            id:'id1',
            name:'john',
            email:'email@example.com'
        },
        {
            id:'id2',
            name:'john',
            email:'email2@example.com'  
        }
    ],selected:[],
    selectAll:false
   }),
   methods :{
    select(){
        this.selected =[];
        if (!this.selectAll) {
           for (let i in this.items) {          
            this.selected.push(this.items[i].id);              
            
           } 
        }
    }
   }
})
</script>

<template>
    <table class="table table-boardered table-stripped">
        <thead>
            <tr></tr>
        </thead>
    </table>
</template>