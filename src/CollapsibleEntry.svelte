<script>
    export let isCollapsed;
    export let data;
    import {Collapse} from 'bootstrap' ;
import { onMount } from 'svelte';

    let collapsible;
    let collapse;
    onMount(()=>{
        console.log(collapsible);
        collapse = new Collapse(collapsible, {
            toggle: false
        })
        // collapse.hide()
    })

    function moped(){
        console.log("soos");
        collapse.show()
    }
    
    $: {
        if ( collapse) {
            isCollapsed ? collapse.hide() : collapse.show();
        }
    }
</script>



<div class="card">
    <div class="card-header " on:click>
      soos

    </div>
    <div class="collapse"  bind:this={collapsible} >
      <div class="card-body">
        saas
      </div>
    </div>
    
  </div>