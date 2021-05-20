<template>
  <div class="content">
   <ul>
  <li v-for="noten in noten">{{noten.name, noten.grades}} </li>
  
  </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: function(){
    return{


  noten:[

    {
        name: "Mathematik",
        grades: [5,4.7,3.5,4.1] 
    },
    {
        name: "Geschichte",
        grades: [5.5,4.9,5.75] 
    },
    {
        name: "Physik",
        grades: [2,2.7,4.3] 
    },
    {
        name: "Deutsch",
        grades: [4.25,4.1,3.5] 
    },
]

    }
  }
}
</script>

<style lang="scss">
.content{
width: 100px;
margin: 0 auto;
} 
</style>
