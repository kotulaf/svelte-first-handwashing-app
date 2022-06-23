<script>
    import ProgressBar from "./ProgressBar.svelte";
</script>

<style>
   h2 {
    font-size: 25px;
   } 

   .start {
    margin: 1% 2%;
   }

   .start-btn {
    width: 100%;
   }
</style>

<div class="container-fluid text-basic">
    <h2>Seconds Left: </h2>
</div>

<div class="container-fluid">
    <div class="start">
        <button class="btn btn-outline-primary start-btn">Start</button>
    </div>
</div>

<ProgressBar />