<template>
  <div id="app">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">

    <Student :message="desc" :todos="talabalar">



      <form class="w-50 m-5">
         <div class="form-group">
           <label for="">name</label>
           <input type="text" class="form-control" v-model="newName">
         </div>

        <div class="form-group">
          <label for="">surname</label>
          <input type="text" class="form-control" v-model="newSurname">
        </div>

        <div class="form-group">
          <label for="">age</label>
          <input type="text" class="form-control" v-model="newAge">
        </div>

        <button type="button" @click="add" class="btn btn-primary">button</button>
      </form>



    </Student>

  </div>
</template>

<script>

import Student from "@/components/lesson2/Student";

export default {
  name: 'App',

  methods:{
     add(){
        this.talabalar.push({
          name: this.newName,
          surname: this.newSurname,
          age: this.newAge
        }),
          this.newName='',
          this.newSurname='',
          this.newAge=''
     }
  },
  data(){
    return{
      newName:'',
      newSurname:'',
      newAge:'',
      desc:"lorem ipsum dolor sit amet, consectetur",

      talabalar:[
        {
           name:"ali",
           surname:"valiyev",
           age:32
        },
        {
          name:"vali",
          surname:"valiyev",
          age:32
        },
        {
          name:"sardor",
          surname:"valiyev",
          age:32
        },
        {
          name:"alisher",
          surname:"valiyev",
          age:32
        },
        {
          name:"sherali",
          surname:"valiyev",
          age:32
        }
      ]
    }
  },
  components: {
    Student
  }
}
</script>



