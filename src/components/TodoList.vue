<template>
    <div class="todoList">
        <h4>Your's Todo's:</h4>
        <div class="todos">
            <ul v-if="todos.length != 0">
                <li class="task" v-for="todo in todos" v-bind:key="todo">
                    {{todo}} <br>
                </li>
            </ul>
            <div v-else style="font-size: 12px">
                You have no tasks! <br>
                Add one
            </div>
        </div>
        <form @submit="onSubmit">
            <input type="text" placeholder="Learn VueJS" v-model="task">
            <br>
            <input type="submit" value="Add Task">
        </form>
        <span v-if="error">
            {{error}}
        </span>
    </div>
</template>
<style scoped>
.todoList{
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    width: 60%;
}
.todos{
    width: 300px;
    margin-left: auto;
    margin-right: auto;
}
.task{
    text-align: center;
}
</style>
<script>
export default {
    data() {
        return {
            error: '',
            task: '',
            todos: [],
        }
    },
    methods: {
        mounted(){
            
        },
        onSubmit(event) {
            event.preventDefault()
            if (this.task){
                this.todos.push(this.task)
                this.error = ''
                this.task = ''
            }
            else
                this.error = "Your task can't be empty!"
        }
    }
}
</script>