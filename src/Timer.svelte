<script>
    import ProgressBar from "./ProgressBar.svelte";
    let percentage = 100;
</script>

<style>
   h2 {
    font-size: 25px;
   } 

   .start {
    margin: 1% 0;
   }

   .start-btn {
    width: 100%;
   }
</style>

<div class="container">
    <div class="row">
      <div class="col">
      </div>
      <div class="col">
        <div class="text-basic">
            <h2>Seconds Left: </h2>
        </div>
        
        <ProgressBar {percentage}/>
            <div class="start">
                <button class="btn btn-outline-primary start-btn">Start</button>
            </div>
      </div>
      <div class="col">
      </div>
    </div>
  </div>

