<template>

  <div>

    <img src="https://images.pexels.com/photos/112460/pexels-photo-112460.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500" alt="">

    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad assumenda aut blanditiis dicta ea eos harum, iste laborum laudantium magni nisi nobis officiis, porro quae quidem sunt vitae voluptas voluptates.
    </p>

    <slot :data="data">

    </slot>
  </div>
</template>

<script>

export default {
   data(){
     return{
       data:"bu mening birinchi ishim"
     }
   }
}
</script>
