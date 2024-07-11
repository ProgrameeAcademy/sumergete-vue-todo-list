<template>
  <div id="aplicacion">
    <h1>TODO LIST</h1>
    <small>by <a href="https://academia.programee.com">programee</a></small>
    <div class="contenido">
      <!-- Formulario para agregar una nueva tarea -->
      <div class="add-todo">
        <!-- Campo de entrada para la nueva tarea -->
        <input type="text" placeholder="Añadir una nueva tarea" />
        <!-- Botón para agregar la tarea -->
        <button>Añadir</button>
      </div>
      <!-- Lista de tareas -->
      <ul>
        <!-- Aquí debes renderizar las tareas con un bucle (v-for?) -->
        <!-- Cada tarea debe tener un texto, un botón para eliminarla y una manera de marcarla como completada -->
        <li>
          <!-- Texto de la tarea -->
          <span>Ejemplo</span>
          <!-- Botón para completar la tarea -->
          <button class="green">Completar</button>
          <!-- Botón para eliminar la tarea -->
          <button>Eliminar</button>
        </li>
      </ul>
    </div>
  </div>

</template>

<script setup>
// Importar la función ref desde Vue
import { ref } from 'vue';

// Definir una lista de tareas inicial
const todos = ref([
  { id: 1, text: 'Aprender Vue.js', completed: false },
  { id: 2, text: 'Dejar una reseña en el curso', completed: false },
  { id: 3, text: 'Terminar este primer proyecto', completed: false },
]);

// Definir un valor reactivo para la nueva tarea
const newTodo = ref('');

// Función para agregar una nueva tarea
const addTodo = () => {
  // TODO: Completar la función para agregar una tarea
  // Tips:
  // - Verificar que el campo de la nueva tarea no esté vacío
  // - Agregar la nueva tarea a la lista 'todos' con un id único y 'completed' como false
  // - Limpiar el campo de la nueva tarea después de agregarla
};

// Función para marcar una tarea como completada o no completada
const toggleComplete = (id) => {
  // TODO: Completar la función para marcar una tarea como completada o no
  // Tips:
  // - Encontrar la tarea en la lista 'todos' usando el id
  // - Alternar el valor de 'completed' de la tarea
};

// Función para eliminar una tarea de la lista
const deleteTodo = (id) => {
  // TODO: Completar la función para eliminar una tarea
  // Tips:
  // - Filtrar la lista 'todos' para excluir la tarea con el id proporcionado
};
</script>

<style>
#aplicacion {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
  width: 100%;
}

.add-todo {
  margin-bottom: 20px;
}

.add-todo input {
  padding: 10px;
  font-size: 16px;
  width: 200px;
  margin-right: 10px;
}

.add-todo button {
  padding: 10px;
  font-size: 16px;
}

.contenido {
  display: flex;
  width: 100%;
  flex-direction: column;
  margin-top: 20px;
  gap: 30px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px;
  font-size: 18px;
  border-bottom: 1px solid #ccc;
}

li.completed span {
  text-decoration: line-through;
  color: gray;
}

li button {
  background: none;
  border: none;
  color: red;
  cursor: pointer;
}

li button-green {
  color: aquamarine;
}
</style>
