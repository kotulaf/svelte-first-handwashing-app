<script>
    import Timer from "./Timer.svelte";
    import HowTo from "./HowTo.svelte";
    let audio;
    function timerEnds() {
        audio.play();
    }
</script>

<style>
    h1 {
        text-align: center;
        margin: 2% 2%;
    }
</style>

<h1 class="text-basic">Handwashing App</h1>

<Timer on:end={timerEnds} />
<HowTo />

<audio bind:this={audio}>
    <source src="sound.wav">
</audio>