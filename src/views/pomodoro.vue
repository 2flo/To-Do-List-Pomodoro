<template>
  <div class="timer">
    <h1>Pomodoro</h1>
    <button @click="timer">Lancer le décompte</button>
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
            }
        }
    }
}
</script>