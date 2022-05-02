<template>
  <div class="root">
    <div class="container">
      <TodoList/>
    </div>
    <footer class="footer">
      <a href="http://github.com/majorek31">Source code</a>
    </footer>
  </div>
</template>

<script>
import TodoList from "./components/TodoList.vue"
export default {
  name: 'App',
  components: {
    TodoList
  }
}
</script>
<style>
body{
  font-family: Verdana,Geneva,sans-serif; 
  background-color: #fffaf7;
}
.container{
  width: 800px;
  margin-left: auto;
  margin-right: auto;
}
.footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  text-align: center;
}
a:link{
  text-decoration: none;
}
a:visited{
  text-decoration: none;
}
</style>