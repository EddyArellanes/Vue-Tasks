<template>
  <v-card color="white" raised>
   <v-card-title primary-title>
      <div>
        <h3 class="headline mb-0">{{title}}</h3>        
      </div>
      <div>{{description}}</div>
    </v-card-title>
    <v-card-actions>
        <v-btn
        color="green darken-2"
        class="white--text"                  
      >
        Editar
        <v-icon right dark>edit</v-icon>
      </v-btn>
                        <v-btn
        color="red darken-2"
        class="white--text"                  
      >
        Eliminar
        <v-icon right dark>delete</v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  name: 'Task',
  props:{
    title: String,
    description: String
  }
}
</script>

