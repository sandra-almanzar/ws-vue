<template>
    <div>
        <div class="card-body p-2 p-md-3">
            <div class="row align-items-center">
                <div class="justify-content-center align-items-center col-md-1 col-3">
                    <img v-bind:src="img" >
                </div>
                <div class="col-md-11 col-9">
                    <div class="row align-items-center">
                        <div class="mb-2 col">
                            <h2>{{ job.name }}</h2>
                        </div>
                    </div>
                </div>

            </div>
            <div class="row flex-colum">
                <div>
                    <span>{{ job.company }}</span>
                </div>
                <div>
                    <span>{{ job.city }}</span>
                </div>
                <div>
                    <span>{{ job.salary }}</span>
                </div>
                <div>
                    <span>{{ job.vacancies }}</span>
                </div>
                <div>
                    <span>{{ job.calendar }}</span>
                </div>

            </div>
            
        </div>
    </div>
    
  </template>
  
  <script>
  export default {
    name: 'job-card',
    props:{
        job: String
    },
};
  </script>