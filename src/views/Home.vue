<template>
  <div class="home">
    <Introduction/>
    <Todo/>
    <Credits/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Todo from '@/components/Todo.vue'
import Introduction from '@/components/Introduction.vue'
import Credits from '@/components/Credits.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    Todo,
    Introduction,
    Credits,
    Footer
  }
}
</script>
