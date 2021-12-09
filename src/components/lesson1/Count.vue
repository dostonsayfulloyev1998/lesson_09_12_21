<template>
  <div class="one">
          <h1> Counter:{{count}}  </h1>
          <button class="btn btn-primary mx-2" @click="plus">plus</button>
    <button class="btn btn-danger" @click="minus">minus</button>

    <slot></slot>
  </div>
</template>

<script>

export default {
         data(){
           return{
               count:0
           }
         },
       methods:{
          plus(){
              this.count++
          },
         minus(){
            if (this.count>0)
              this.count--
         }
       }
    }

</script>

<style>

.one{
    border:1px solid black;
    margin: 20px;
  padding: 15px;
  border-radius:10px;
}
</style>
