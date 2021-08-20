<template>
  <div id="app" class="container">
    <h1 class="text-center my-5">Tabla de usuarios</h1>
    <table class="table table-striped table-hover text-center">
      <thead>
        <tr>
          <th scope="col">Nombre</th>
          <th scope="col">Apellido</th>
          <th scope="col">RUN</th>
          <th scope="col">Fecha de Nacimiento</th>
          <th scope="col">Edad</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(obj,index) in array" :key="index">
          <td v-for="(item, name, index2) in obj" :key="index2">{{item}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name:'Tabla',
  data(){
    return {
      array:[
        { 
          nombre: 'nombre01',
          apellido: 'apellido01',
          run: '11.111.111-1',
          fechaNacimiento: '01-01-2001',
          edad: 10
        },
        {
          nombre: 'nombre02',
          apellido: 'apellido02',
          run: '22.222.222-2',
          fechaNacimiento: '02-02-2002',
          edad: 9
        },
        {
          nombre: 'nombre03',
          apellido: 'apellido03',
          run: '33.333.333-3',
          fechaNacimiento: '03-03-2003',
          edad: 8
        }
      ]
    }
  }
}
</script>
