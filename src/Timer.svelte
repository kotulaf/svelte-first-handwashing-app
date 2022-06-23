<script>
    import { createEventDispatcher } from "svelte";
    import ProgressBar from "./ProgressBar.svelte";
    const totalSeconds = 20;
    const addPercentage = 100 / totalSeconds;
    let secondsLeft = totalSeconds;
    let percentage = 0;

    const dispatch = createEventDispatcher();

    let isRunning = false;
    function startTimer() {
        const interval = setInterval(() => {
            isRunning = true;
            secondsLeft -= 1; 
            percentage += addPercentage; 
            if(secondsLeft == 0)
            {
                clearInterval(interval);
                /* location.reload(); */
                isRunning = false;
                percentage = 0;
                secondsLeft = totalSeconds;
                dispatch("end");
            }  
        }, 1000);
    }
</script>

<style>
   h2 {
    font-size: 25px;
   } 

   .start {
    margin: 5% 0;
   }

   .start-btn {
    width: 100%;
   }

   .start-btn[disabled] {
    cursor: not-allowed;
   }
</style>

<div class="container">
    <div class="row">
      <div class="col">
      </div>
      <div class="col">
        <div class="text-basic">
            <h2>Seconds Left: {secondsLeft}</h2>
        </div>
        
        <ProgressBar {percentage}/>
            <div class="start">
                <button disabled={isRunning} on:dblclick={startTimer} class="btn btn-outline-primary start-btn" id="start-button">Start</button>
            </div>
      </div>
      <div class="col">
      </div>
    </div>
  </div>

