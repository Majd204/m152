<template>
  <div class="content">

  <ul>
  <li v-for="todo in todos">{{todo}} </li>
  </ul>
  
  <input v-model="newTodo"/>
  <button v-on:click="addTodo()">Hinzufügen</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function(){
    return{

      todos:[ 'Helloworld',
              'bibabu',
              'wasus'

  
      ],
      newTodo:''
    }
  },
  methods:{
    addTodo: function(){
      this.todos.push(this.newTodo);
      this.newTodo = '';
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