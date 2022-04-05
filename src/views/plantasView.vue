<template>
  <div>
    <div> 
        <h4 class='cyan-text left'>Plantas</h4>
        <a class="waves-effect waves-light btn-small right"><i class="material-icons left">add</i>Agregar</a>
    </div>

    <div>
      <table>
        <thead>
          <tr>
              <th>Codigo</th>
              <th>Nombre Común</th>
              <th>Nombre Cient. </th>
              <th>Familia</th>
              <th>Imagen</th>
          </tr>
        </thead>

        <tbody>
          <tr  v-for="(planta,index) in plantas" :key=index >
            <td>{{planta.codigo}}</td>
            <td>Eclair</td>
            <td>$0.87</td>
            <td>Eclair</td>
            <td>$0.87</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'
  export default{

    data(){
      return {
        plantas:[],
        cantidad:4
      }
    },
    methods:{
      getPlantas(){
        axios.get("http://192.168.88.66:3000/plantas/show").then((result) => {
          this.plantas = JSON.stringify(result.data);
          console.log(result.data);
        })
      },

    },
    created(){
      this.getPlantas()
    }
  }
</script>

