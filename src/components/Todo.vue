1<template>
  <div class="hello">
    <div class="container my-5 ">
    <!-- Section: Block Content -->
    <section>    
      <div class="row">
        <div class="col-12">
          <div class="card card-list">
            <div class="card-header white d-flex justify-content-between align-items-center py-3">
              <p class="h5-responsive font-weight-bold mb-0">Your Bucketlist</p>
            </div>
            <div class="container my-5">
                  <div class="col-md-12 mb-4">
                    <input @keyup.enter="addTodo()" v-model="userInput" type="text" id="subject" class="form-control" placeholder="Type and press enter">
                  </div>
            </div>
              <table class="table">
                <thead>
                  <tr>
                    <th scope="col">Task</th>
                    <th scope="col">Action</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="(todo,index) in todos" :key="todo.title">
                    <th scope="row">{{todo}}</th>
                    <td v-if="index > 0" @click="removeTodo(index)">remove</td>
                  </tr>
                </tbody>
              </table>
          </div>
        </div>
      </div>
    </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Todo',
  props: {    
    msg: String,
  },
  data: function() {
    return{
      userInput:'',
      todos:[
            ''
          ]
        }
    },
  methods:{
    addTodo(){
      if(this.userInput!=""){        
        console.log("adding");
        this.todos.push(this.userInput)
        this.userInput=""
      }
    },
    removeTodo(id){
      console.log("removing");
      this.$delete(this.todos, id);
    }
  }
}
</script>
<style>
  .border-top {
      border-top: 5px solid #33b5e5 !important;
      border-top-left-radius: .25rem!important;
      border-top-right-radius: .25rem!important;
    }
</style>
