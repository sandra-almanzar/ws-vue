<template>
  <div id="app">
    <div v-for="(job, index) in jobs" :key="index">
      <job-card :job="job"/>
    </div>
  </div>
</template>

<script>
import JobCard from './components/JobCard.vue';

export default {
  name: 'App',
  components: {
    'job-card': JobCard,
  },
  data(){
    return {
      jobs: [
        {
            name: 'Ejecutivo Comercial Barranquilla',
            img: '../assets/company.sgv',
            requirements: ['B2B Sales'],
            company: 'Skla Consulting',
            city: 'Barranquilla',
            salary: '1.8M - 2M COP',
            vacancies: '1 Vacante',
            calendar: '5 days ago',
        },
        {
            name: 'Ejecutivo Comercial Cali',
            img: '../assets/company.sgv',
            requirements: ['Commercial Analysis','Field Work','B2b Sales'],
            company: 'Skla Consulting',
            city: 'Santiago de Cali',
            salary: '1.8M - 2M COP',
            vacancies: '1 Vacante',
            calendar: '5 days ago',
        },
        {
            name: 'Desarrollador fullstack',
            img: '../assets/company.sgv',
            requirements: ['React','Typescript','.Net(C #)'],
            company: 'Skla Consulting',
            city: 'Hybrid - mix remote and in office (Bogotá)',
            salary: '5M - 7M COP',
            vacancies: '1 Vacante',
            calendar: '5 days ago',
        },
        {
            name: 'Líder técnico de desarrollo',
            img: '../assets/company.sgv',
            requirements: ['Javascript','React','C#'],
            company: 'Skla Consulting',
            city: 'Hybrid - mix remote and in office (Bogotá)',
            salary: '13M - 15M COP',
            vacancies: '1 Vacante',
            calendar: '5 days ago',
        },
        {
            name: 'Desarrollador web',
            img: '../assets/DATACRM_logo.png',
            requirements: ['Laravel','Seo','Javascript'],
            company: 'DATACRM',
            city: 'Remote',
            salary: '3M - 3.5M COP',
            vacancies: '1 Vacante',
            calendar: '6 days ago',
        },
        {
            name: 'Ejecutivo Comercial Servicios Salud',
            img: '../assets/asosalud.png',
            requirements: ['Business Closing','Businnes Development','Cold Prospecting'],
            company: 'Asosalud Ltda',
            city: 'Bogotá',
            salary: '1.9M - 3M COP',
            vacancies: '1 Vacante',
            calendar: '6 days ago',
        },
        {
            name: 'Lider Administrativo',
            img: '../assets/OIT.png',
            requirements: ['Niif','Financial Analysis','Accounting'],
            company: 'OIT AVIATUR',
            city: 'In Office ()',
            salary: '4.5M - 5M COP',
            vacancies: '1 Vacante',
            calendar: '6 days ago',
        },

        ],

    
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
