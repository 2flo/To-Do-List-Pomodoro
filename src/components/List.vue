<template>
    <div class="list">
        <div class="list_title">{{title}}
           <div class="list_body">
              <div class="task">
                  <input type="search">
                  <button @click="addTaskes">Ok</button>
                  <input type="checkbox" @click="removeTaskes">
                  {{task.text}}
              </div>
           </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "List",
    props: ['title'],
    data: function(){
        return{
            task: [{text: ""}]
        }
    },
    methods: {
        addTaskes: function(){
            this.task.push({text: this.newTask});
            this.newTask= "";
        },
        removeTaskes: function(){
            this.task.pop({text: this.newTask});
        }
    }
}

</script>

<style>
.list{
    background-color: blueviolet;
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-around;
    width: 30vw;
    height: 40vh;
}

.list_title{
    text-align: center;
    color: black;
    font-size: 2em;
}

.task{
    display: flex;
    flex-direction: column;
}

button{
    width: 5vw;
}
</style>