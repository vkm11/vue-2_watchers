<template>
<div>
  <h1>{{count}}</h1>
  <button v-on:click="count=count+1"> + </button>

  <button v-on:click="count=count-1"> - </button>
</div>
</template>

<script>
export default {
    name:"Watcher-Home",
    data(){
        return{
            count:0
        }
    },
    watch:{
        count(val, prev){
            if(val>5 && val>prev){
                this.count=0
                // alert("stop counting")
            }
        }
    }
}
</script>

<style>

</style>