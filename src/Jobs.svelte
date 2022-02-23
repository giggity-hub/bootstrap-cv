<script>
    import cv from './data/cv.json';
import Branch from './lib/Branch.svelte';

cv.sort((a,b) => (a.from > b.from) ? 1 : -1)

</script>
<div class="accordion  " id="cv-accordion">
{#each cv as job, i }
    <div class="row g-0  w-100 mx-center">
        <h2 class="col-2 col-md-3 pe-5 text-end text-primary mt-2 ">
            {new Date(job.from).getFullYear()}
        </h2>

        <div class="col  d-flex">
            <div class="border border-1 bg-primary " style="width:0;"  >
                <div class="marker mt-4"></div>
            </div>
            
            <div class="ms-5 accordion-item flex-grow-1 mb-4 border-0">
                <h2 class="accordion-header" id="heading-{i}">
                  <button class="accordion-button rounded-3" type="button" data-bs-toggle="collapse" data-bs-target="#collapse-{i}" aria-expanded="true" aria-controls="collapse-{i}">
                    <span class="fs-4">{job.title}</span>
                    <span class="badge rounded-pill ms-3 d-none d-md-inline {job.category}">{job.category}</span>
                    
                  </button>
                  
                </h2>
                <div id="collapse-{i}" class="accordion-collapse collapse " aria-labelledby="headingOne" data-bs-parent="#cv-accordion">
                  <div class="accordion-body">
                      <p class="text-muted"></p>
                      <h5 class="fw-normal text-secondary">Beschreibung</h5>
                      <p>{job.description}</p>
                      <h5 class="fw-normal text-secondary">Was habe ich gelernt?</h5>
                      <p>{job.reflection}</p>
                      <span class="text-muted d-none d-md-inline">{job.from} bis {job.to}</span>
                  </div>
                </div>
              </div>
        </div>
    </div>
{/each}
</div>

<style>

.badge.work{
    background: var(--bs-indigo)
}
.badge.education{
    background: var(--bs-blue)
}
.badge.volunteering{
    background: var(--bs-pink)
}

.marker{
    width: 1rem;
    height: 1rem;
    background: white;
    transform: translateX(-50%);
    border-radius: 50px;
}
/* .branch{
    background: orange;
}
.branch:nth-child(even){
    background: red;
    flex-direction: row-reverse;
} */
</style>