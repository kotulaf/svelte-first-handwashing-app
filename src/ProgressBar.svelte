<script>
    export let percentage;
</script>

<style>

    .progress {
        margin: 0;
        width: 100%;
    }

</style>

<div class="progress">
    <div class="progress-bar progress-bar-striped progress-bar-animated bg-info" role="progressbar" style="width: {percentage}%" aria-valuenow={percentage} aria-valuemin="0" aria-valuemax="100"></div>
</div>