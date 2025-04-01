<script>
export default {
  data() {
    return {
      horarioAcademico: [
        { hora: '11:00-13:00', lunes: 'Redes de Computadoras', martes: '', miercoles: 'Redes de Computadoras', 
        jueves: 'Lenguajes y Autómatas I', viernes: 'Lenguajes y Autómatas I' },
        { hora: '12:00-14:00', lunes: '', martes: 'Lenguajes y Autómatas I',
         miercoles: '', jueves: '', viernes: '' },
        { hora: '13:00-15:00', lunes: 'Ingeniería de Software', martes: '', miercoles: '', 
        jueves: 'Administración de Bases de Datos', viernes: 'Redes de Computadoras' },
        { hora: '14:00-15:00', lunes: '', martes: '', miercoles: '', jueves: '', 
        viernes: 'Ingeniería de Software' },
        { hora: '15:00-17:00', lunes: 'Programación Web', martes: 'Taller de Sistemas Operativos', 
        miercoles: 'Ingeniería de Software', jueves: 'Taller de Sistemas Operativos', viernes: 'Programación Web' },
        { hora: '16:00-17:00', lunes: '', martes: '', miercoles: '', jueves: '', 
        viernes: 'Administración de Bases de Datos' },
        { hora: '17:00-19:00', lunes: 'Administración de Bases de Datos', martes: 'Lenguajes de Interfaz', 
        miercoles: '', jueves: 'Lenguajes de Interfaz', viernes: '' }
      ],
      activeTab: 'academico'
    }
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab
    }
  }
}
</script>

<template>
  <div class="horario-container">
    <h1 class="titulo-horario">Horario Estudiantil</h1>
    
    <div class="tabs">
      <button 
        @click="setActiveTab('academico')" 
        :class="{ active: activeTab === 'academico' }"
      >
        Horario Académico
      </button>
      <button 
        @click="setActiveTab('extracurriculares')" 
        :class="{ active: activeTab === 'extracurriculares' }"
      >
        Actividades Extracurriculares
      </button>
    </div>
    
    <div v-if="activeTab === 'academico'" class="tabla-container">
      <table class="tabla-horario">
        <thead>
          <tr>
            <th>Hora</th>
            <th>Lunes</th>
            <th>Martes</th>
            <th>Miércoles</th>
            <th>Jueves</th>
            <th>Viernes</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(clase, index) in horarioAcademico" :key="index">
            <td>{{ clase.hora }}</td>
            <td>{{ clase.lunes }}</td>
            <td>{{ clase.martes }}</td>
            <td>{{ clase.miercoles }}</td>
            <td>{{ clase.jueves }}</td>
            <td>{{ clase.viernes }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    
    <div v-if="activeTab === 'extracurriculares'" class="tabla-container">
      <table class="tabla-actividades">
        <thead>
          <tr>
            <th>Día</th>
            <th>Actividad</th>
            <th>Participantes Recomendados</th>
            <th>Hora</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(actividad, index) in actividadesExtracurriculares" :key="index">
            <td>{{ actividad.dia }}</td>
            <td>{{ actividad.actividad }}</td>
            <td>{{ actividad.participantes }}</td>
            <td>{{ actividad.hora }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
.horario-container {
  max-width: 1200px;
  margin: 2rem auto;
  padding: 2rem;
  background: rgba(255, 255, 255, 0.95);
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.titulo-horario {
  color: #f5a50f;
  text-align: center;
  margin-bottom: 1.5rem;
  font-size: 2rem;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
}

.tabs {
  display: flex;
  justify-content: center;
  margin-bottom: 2rem;
  gap: 1rem;
}

.tabs button {
  padding: 0.8rem 1.5rem;
  border: none;
  background-color: #e0e0e0;
  border-radius: 25px;
  cursor: pointer;
  font-weight: 600;
  transition: all 0.3s ease;
}

.tabs button.active {
  background-color: #f8b807;
  color: white;
}

.tabs button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.tabla-container {
  overflow-x: auto;
}

.tabla-horario, .tabla-actividades {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
  border-radius: 10px;
  overflow: hidden;
}

.tabla-horario th, 
.tabla-horario td,
.tabla-actividades th,
.tabla-actividades td {
  padding: 1rem;
  text-align: center;
  border: 1px solid #e0e0e0;
}

.tabla-horario th,
.tabla-actividades th {
  background-color: #ffc005;
  color: black;
  font-weight: 600;
}

.tabla-horario tr:nth-child(even),
.tabla-actividades tr:nth-child(even) {
  background-color: #f8f9fa;
}

.tabla-horario tr:hover,
.tabla-actividades tr:hover {
  background-color: #e9f5ff;
}

@media (max-width: 768px) {
  .horario-container {
    padding: 1rem;
    margin: 1rem;
  }
  
  .tabs {
    flex-direction: column;
    align-items: center;
  }
  
  .tabla-horario th, 
  .tabla-horario td,
  .tabla-actividades th,
  .tabla-actividades td {
    padding: 0.5rem;
    font-size: 0.9rem;
  }
}

</style>