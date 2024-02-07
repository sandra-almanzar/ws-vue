<template>
  <div id="app">
    <header>
      <job-menu :menu="menu"></job-menu>
    </header>
    <main class="row">
      <aside class="col-1 p-0 borde-derecho">
        <left-menu :leftMenu="leftMenu"></left-menu>
      </aside>
      <div class="container-fluid col">
        <div v-for="(job, index) in jobs" :key="index">
          <job-card :job="job" />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import JobCard from "./components/JobCard.vue";
import JobMenu from "./components/JobMenu.vue";
import LeftMenu from "./components/LeftMenu.vue";

export default {
  name: "App",
  components: {
    "job-card": JobCard,
    "job-menu": JobMenu,
    "left-menu": LeftMenu,
  },
  data() {
    return {
      jobs: [
        {
          name: "Ejecutivo Comercial Barranquilla - Experiencia en turismo",
          img: require(`@/assets/company.svg`),
          requirements: ["B2B Sales", "commercial analysis", "field work"],
          company: "Skla Consulting",
          city: "Barranquilla",
          salary: "1.8M - 2M COP",
          vacancies: "1 Vacante",
          calendar: "5 days ago",
        },
        {
          name: "Ejecutivo Comercial Cali",
          img: require(`@/assets/company.svg`),
          requirements: ["commercial analysis", "field work", "b2b sales"],
          company: "Skla Consulting",
          city: "Santiago de Cali",
          salary: "1.8M - 2M COP",
          vacancies: "1 Vacante",
          calendar: "5 days ago",
        },
        {
          name: "Desarrollador fullstack",
          img: require(`@/assets/company.svg`),
          requirements: ["React", "Typescript", ".Net(C #)"],
          company: "skla Consulting",
          city: "Hybrid - mix",
          salary: "5M - 7M COP",
          vacancies: "1 Vacante",
          calendar: "5 days ago",
        },
        {
          name: "Líder técnico de desarrollo",
          img: require(`@/assets/company.svg`),
          requirements: ["Javascript", "React", "C#"],
          company: "Skla Consulting",
          city: "Hybrid - mix",
          salary: "13M - 15M COP",
          vacancies: "1 Vacante",
          calendar: "5 days ago",
        },
        {
          name: "Desarrollador web",
          img: require(`@/assets/DATACRM_logo.png`),
          requirements: ["Laravel", "Seo", "Javascript"],
          company: "DATACRM",
          city: "Remote",
          salary: "3M - 3.5M COP",
          vacancies: "1 Vacante",
          calendar: "6 days ago",
          tooltipIcons: [
            {
              icon: "bi bi-people",
              tooltip: "Ambiente de trabajo amigable",
            },
            {
              icon: "bi bi-calendar-plus",
              tooltip: "Flexibilidad de horarios",
            },
          ],
        },
        {
          name: "Ejecutivo Comercial Servicios Salud",
          img: require(`@/assets/asosalud.png`),
          requirements: [
            "Business Closing",
            "Businnes Development",
            "Cold Prospecting",
          ],
          company: "Asosalud Ltda",
          city: "Bogotá",
          salary: "1.9M - 3M COP",
          vacancies: "1 Vacante",
          calendar: "6 days ago",
        },
        {
          name: "Lider Administrativo",
          img: require(`@/assets/OIT.jpg`),
          requirements: ["Niif", "Financial Analysis", "Accounting"],
          company: "OIT AVIATUR",
          city: "In Office ()",
          salary: "4.5M - 5M COP",
          vacancies: "1 Vacante",
          calendar: "6 days ago",
        },
      ],
      menu: [
        "Empleos",
        "Bootcamp",
        "Sobre nosotros",
        "Para profesionales",
        "Para empresas",
      ],
      leftMenu: [
        { icono: "bi bi-briefcase", nombre: "Empleos" },
        { icono: "bi bi-file-earmark-check", nombre: "Postulaciones" },
        { icono: "bi bi-controller", nombre: "Cursos" },
        { icono: "bi bi-chat-text", nombre: "Preguntas" },
        { icono: "bi bi-braces", nombre: "Bootcamp" },
        { icono: "bi bi-gem", nombre: "Premios" },
        { icono: "bi bi-file-earmark-person", nombre: "Tu CV" },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: "Montserrat", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
}
.borde-derecho {
  border-right: 1px solid #dee2e6 !important;
}
</style>
