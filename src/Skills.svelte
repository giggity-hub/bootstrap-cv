<script>
    import skills from './data/skills.json'
</script>




{#each skills as subject}

 <div class="mb-5 border border-3 p-3 pt-4 rounded position-relative ">
  <h5 class=" px-3 position-absolute top-0 translate-middle-y" style="background: var(--bs-body-bg);" >
    {subject.title}
  </h5>
  {#each subject.entries as entry }


  <div class="row align-items-center mb-2 px-md-5 pt-2 ">
    <div class="col col-sm-4 col-md-2  d-flex justify-content-end ">
      <div>{entry.name}</div> 
      <div class=" text-end text-primary" style="width: 4rem">
        {entry.confidence}/10
      </div>
    </div>
    <div class="col">
      <div class="progress ">
        <div class="progress-bar bg-primary " role="progressbar" style="width: {entry.confidence*10}%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
      </div>
    </div>
  </div>
  {/each}
 </div>
{/each}
