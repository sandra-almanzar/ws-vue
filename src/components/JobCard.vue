<template>
  <div class="my-container mb-3 border">
    <div class="card-body p-2 p-md-3">
      <div class="row align-items-center">
        <div
          class="d-flex justify-content-center align-items-center col-md-1 col-3"
        >
          <img
            :src="job.img"
            alt="Company logo"
            width="70"
            height="70"
            class="rounded"
          />
        </div>
        <div class="col-md-11 col-9">
          <div class="row align-items-center">
            <div class="mb-2 col ps-0">
              <a
                href="#"
                class="container-fluid text-dark d-inline d-md-inline-flex text-decoration-none"
              >
                <h1 class="font-weight-bold pl-md-2 pr-md-2 mb-0 pb-0 me-3">
                  {{ job.name }}
                </h1>
                <section
                  class="pl-md-2 d-inline d-md-inline-flex align-items-center text-truncate"
                >
                  <div
                    class="text-truncate border border-dark text-dark text-capitalize m-1 p-1 rounded-2"
                    style="font-size: 0.8em"
                    v-for="(requirement, index) in job.requirements"
                    :key="index"
                  >
                    <span>{{ requirement }}</span>
                  </div>
                </section>
              </a>
            </div>
          </div>
          <div
            class="row container-fluid pl-md-2 mt-1 flex-column flex-md-row"
            style="font-size: 0.9em"
          >
            <div
              class="text-truncate text-capitalize col d-flex justify-content-start ms-0 ps-0"
            >
              <i class="bi bi-buildings pe-1"></i>
              <span class="pe-2">{{ job.company }}</span>
            </div>
            <div class="text-truncate col d-flex justify-content-start">
              <i class="bi bi-geo-alt pe-1"></i>
              <span>{{ job.city }}</span>
            </div>
            <div class="text-truncate col d-flex justify-content-start">
              <i class="bi bi-cash-stack pe-1"></i>
              <span>{{ job.salary }}</span>
            </div>
            <div class="text-truncate col d-flex justify-content-start">
              <i class="bi bi-people pe-1"></i>
              <span>{{ job.vacancies }}</span>
            </div>
            <div class="text-truncate col d-flex justify-content-start">
              <i class="bi bi-calendar3 pe-1"></i>
              <span>{{ job.calendar }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "job-card",
  props: {
    job: String,
  },
};
</script>
<style>
h2 {
  font-family: Montserrat, sans-serif;
}
.my-container:hover {
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
}
</style>
