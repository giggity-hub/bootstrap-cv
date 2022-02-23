<script>
  import logo from './assets/svelte.png'
  import Counter from './lib/Counter.svelte'
  import styles from './custom.scss';

  import cv from './data/cv.json';
  import '../node_modules/bootstrap/dist/js/bootstrap';
  import '../node_modules/@fortawesome/fontawesome-free/css/all.min.css'
import Skills from './Skills.svelte';
import Jobs from './Jobs.svelte';
import Showcase from './Showcase.svelte';

</script>
<div class="h-screen vh-100 position-relative d-flex flex-column hero-gradient p-5 justify-content-between">
  
  <h1 class="hero-text text-secondary">Moin Leude</h1>
  <h1 class="hero-text text-primary align-self-end text-end">Stefan hier</h1>
  <!-- <img src="/dude.jpg" class="mh-100 img-fluid1position-absolute top-0 end-0" alt="..."> -->

  <!-- <div class=" position-absolute w-100 h-100 top-0 hero-gradient">

  </div> -->
  
</div>
<div class="container">




<section class="mb-5">
  <h1 class="text-primary">Skills</h1>
  <p class="mb-5 mt-3">
      Hier sind ein paar meiner Fähigkeiten und arbiträre subjektive Einschätzung des Skill Levels
  </p>
  <Skills/>
  
</section>

<section class="mb-5">
  <h1 class="text-primary">Projects</h1>
  <p class="mb-5 mt-3">
      Projekte an denen ich arbeite. Ich weiß die meißten sind nicht fertig und sehen aus wie Müll aber irgendwie muss ich hier ja Platz füllen.
  </p>
  <Showcase/>
</section>

<section class="mb-5">
  <h1 class="text-primary">CV</h1>
  <p class="mb-5 mt-3">
    Jobs, Bildung und ehrenamtliche Tätigkeiten
  </p>
  <Jobs/>
</section>

  



  <!-- <div class="d-flex">
    <div class="flex-grow-1 bg-primary">
      soos
    </div>
    <div class="bg-secondary" style="width:.2rem">
    </div>
    <div class="flex-grow-1 bg-primary" id="collapsibles">
      <div class="bg-black relative mw-100">
        <div class="accordion" id="accordionExample">
          {#each cv as item, i }
            <div class="accordion-item">
              <h2 class="accordion-header" id="heading-{i}">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapse-{i}" aria-expanded="true" aria-controls="collapseOne">
                  Accordion Item #1
                </button>
              </h2>
              <div id="collapse-{i}" class="accordion-collapse collapse " aria-labelledby="headingOne" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <strong>This is the first item's accordion body.</strong> It is shown by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
                </div>
              </div>
            </div>
          {/each}
        </div>
      </div>

        
    </div>
  </div> -->


</div>

<style>



  /* .moped{
    flex-grow: 1;
    text-align: center;
    background-color: rgba(0,0,0,0.4);
    color: rgb(233, 233, 233);
    padding: .5rem;
  }

  .moped:hover{
    background-color: rgba(0,0,0,0.5);
  } */
</style>