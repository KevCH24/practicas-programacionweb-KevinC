<script>
    export default{
        data(){
            return{
                //datos de alumnos
                alumnos:[
                    {id:12345 ,nombre:'Kevin Cruz Hernandez',carrera:'Rap'},
                    {id:12345 ,nombre:'Kevin Cruz Hernandez',carrera:'Rap'},
                    {id:12345 ,nombre:'Kevin Cruz Hernandez',carrera:'Rap'},
                    {id:12345 ,nombre:'Kevin Cruz Hernandez',carrera:'Rap'},
                    {id:12345 ,nombre:'Kevin Cruz Hernandez',carrera:'Rap'},
                ]
            }
        }
    }
</script>
<template>
<div class="container">
    <h3 class="mt-4">Lista de alumnos</h3>
    <ul>
        <li v-for="alumno in alumnos" :key="alumno.nc">
            <strong>
                {{ alumno.nombre }}
                <span class="mx-3"></span>
                {{ alumno.carrera }}
            </strong>
        </li>
    </ul>
</div>
</template>
<style>
h3{
    
    color:rgb(248, 170, 13);
    background-color: black;
     border-radius: 15px;
     padding: 10px;
}
ul{
    list-style-type: none;
    padding: 0%;
}
li{
     color: white;
     background-color: black;
     border-radius: 15px;
     padding: 10px;
     margin: 10px;
}
</style> 