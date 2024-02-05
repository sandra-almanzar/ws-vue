<template>
  <div class="container-fluid bg-white" style="height: 15vh">
    <nav class="navbar shadow px-2 py-0 navbar-light bg-light navbar-expand-lg">
      <a href="#" class="order-0">
        <img height="60" src="../assets/logo-blue.png" alt="logo-peaku" />
      </a>
      <div
        class="order-4 order-md-1 navbar-collapse collapse"
        style="display: none"
      >
        <ul
          class="navbar-nav d-flex justify-content-between align-items-center w-100 px-5"
        >
          <li class="nav-item text-truncate">
            <a href="#" class="aria-current='page' active text-decoration-none">
              <span>Empleos</span>
            </a>
          </li>
          <li class="nav-item text-truncate">
            <a href="#" class="aria-current='page' text-decoration-none">
              <span>Bootcamp</span>
            </a>
          </li>
          <li class="nav-item text-truncate">
            <a href="#" class="aria-current='page' text-decoration-none">
              <span>Sobre nosotros</span>
            </a>
          </li>
          <li class="nav-item text-truncate">
            <a href="#" class="aria-current='page' text-decoration-none">
              <span>Para profesionales</span>
            </a>
          </li>
          <li class="nav-item text-truncate">
            <a href="#" class="aria-current='page' text-decoration-none">
              <span>Para empresas</span>
            </a>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "job-menu",
  props: {},
};
</script>
<style>
span {
  color: black;
  font-size: 18px;
}
</style>
