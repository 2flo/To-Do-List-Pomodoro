<template>
<div class="todo">
    <h1>To-Do Liste</h1>
    <input type="search" placeholder="Ajouter un rappel">
    <button @click="addList">Ok</button>
    <List title="Go to fuck you!"></List>
</div>
</template>

<script>
import List from '../components/List.vue'
export default {
    name: "todolist",
    components:{
        List,
    },
    methods: {
        addList: function(){
            this.List.push({List: this.newTask})
        }
    }
}
</script>