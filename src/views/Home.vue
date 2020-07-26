<template>
  <div class="home">
    <Introduction/>
    <Todo/>
    <Credits/>
  </div>
</template>

<script>
// @ is an alias to /src
import Todo from '@/components/Todo.vue'
import Introduction from '@/components/Introduction.vue'
import Credits from '@/components/Credits.vue'

export default {
  name: 'Home',
  components: {
    Todo,
    Introduction,
    Credits
  }
}
</script>
