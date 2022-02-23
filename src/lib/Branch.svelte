<script>
    export let key;
    export let data;
    export let reverse=false;
</script>


<div class="w-75 accordion-item  mb-3">
    <h2 class="accordion-header" id="heading-{key}">
        <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapse-{key}" aria-expanded="true" aria-controls="collapseOne">
        Accordion Item #1
        </button>
    </h2>
    <div id="collapse-{key}" class="accordion-collapse collapse " aria-labelledby="headingOne" data-bs-parent="#cv-accordion">
        <div class="accordion-body">
        <strong>This is the first item's accordion body.</strong> It is shown by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
        </div>
    </div>
</div>

<div class="circle position-absolute {reverse? 'start-0' : 'end-0'} mt-3" class:reverse>

</div>




<style>
.circle{
    width: 1rem;
    height: 1rem;
    background: orange;
}

.circle.reverse{
    background: red;
}
</style>