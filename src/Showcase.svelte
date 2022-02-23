<script>
    import showcases from './data/showcases.json'
</script>

<div class="row row-cols-1 row-cols-md-2  row-cols-xl-3 g-4">
    {#each showcases as showcase }
      <div class="col d-flex">
        <div class="card overflow-hidden border-0 shadow ">
          <div class="overflow-hidden bg-primary image-container d-flex align-items-center  position-relative" style="height:10rem;">
              <a href={showcase.deployment} target="_blank" class="w-100 img-wrapper">
                <img src={showcase.preview || showcase.deployment} class="img-fluid " alt="...">
              </a>
  
          </div>
          
          <div class="card-body d-flex flex-column justify-content-between">
            <div>
              <h5 class="card-title">
                {showcase.title}
              </h5>
              <p>
                {showcase.description}
              </p>
            </div>
    
            <div class="btn-group w-100">
              <a href={showcase.deployment} class="btn btn-secondary text-white" target="_blank"><i class="fas fa-globe"></i> Deployment</a>
              <a href={showcase.repository} class="btn btn-secondary text-white" target="_blank">
                <i class="fab fa-github"></i> Repository
              </a>
            </div>
            
          </div>
        </div>
      </div>
    {/each}
  </div>


<style>
      .image-container > .img-wrapper{
    transition: all .3s ease;
  }
  .image-container:hover > .img-wrapper{
    transform: scale(1.2);
  }
</style>