<template>
<div class="todo">
    <h1>To-Do Liste</h1>
    <input type="search" placeholder="Ajouter un rappel">
    <button>Ok</button>
    <List></List>
</div>
</template>

<script>
import List from '../components/List.vue'
export default {
    name: "todolist",
    components:{
        List
    }
}
</script>