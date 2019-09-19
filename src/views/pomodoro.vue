<template>
  <div class="timer">
    <h1>Pomodoro</h1>
    <button @click="timer">Lancer le décompte</button>
    <button @click="pause">>||</button>
    <button @click="retour">Revenir à 25</button>
    {{count}}
  </div>
</template>
<script>
export default {
    name: 'pomodoro',
    data: function(){
        return{
            val: "",
            count: 25
        }
    },
    methods: {
        timer: function(){
            this.val = setInterval(this.changeCount, 1000);
        },
        changeCount: function()
        {
            this.count--;
            if (this.count === 0){
                clearInterval(this.val);
                alert("Bonne année!");
            }
        },
        pause: function(){
            clearInterval(this.val);
        },
        retour: function(){
            if (this.count === this.pause){
                return this.count;
            }
        }
    }
}
</script>

<style>
button{
    width: auto;
}
</style>