<template>

   <div>

     <label for="myBrowser">Choose a browser from this list:</label>
     <input list="browsers" v-model="name" id="myBrowser" name="myBrowser">
     <datalist id="browsers" >
       <option value="choose name" disabled/>
       <option :value="item.name"  v-for="item in todos" :key="item"/>
     </datalist>

     <table class="table table-striped">
         <thead>
            <tr>
              <td>name</td> <td>surname</td>  <td>age</td>
            </tr>
         </thead>

        <tbody>
          <tr v-for="item in todos" :key="item">
              <td>{{item.name}}</td>  <td>{{item.surname}}</td>  <td>{{item.age}} </td>
          </tr>
        </tbody>
     </table>

   </div>

</template>

<script>

export default {
  name: "Student",
  // props:["message","todos"],
  props:{
    message: String,
    todos: Array
  },
  data(){
    return{
        title:"this is Student page",
      name:''
    }
  }
}
</script>


