<template>
  <v-app>
    <Header />
      <v-container grid-list-md text-xs-center>
        <v-layout row wrap>
          <v-flex xs12 v-if="hasData">
            <v-card dark color="primary">
              <v-card-text class="px-0">No tienes tareas actualmente, inicia una :D</v-card-text>
            </v-card>
          </v-flex>

          <v-flex xs12 v-else>
            <Task v-for="(task, index) in tasks" v-bind:key="index" :title="task.title" :description="task.description"/> 
          </v-flex>
        </v-layout>
      </v-container>
  </v-app>
</template>

<script>
import Header from './components/Header'
import Task from './components/Task'
export default {
  name: 'App',
  components: {
    Header,
    Task
  },
  data () {
    return {
      tasks: [
        {
          title: 'Task 1',
          description: 'Dummy Only :D'
        },
        {
          title: 'Task 2',
          description: 'wawawawa wawawawa wawawawa wawawawawawawawawawawawa wawawawa wawawawa '
        }
      ],
      hasData: false
    }
  }
}
</script>
