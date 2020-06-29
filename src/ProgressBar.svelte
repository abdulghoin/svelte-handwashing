<script>
  export let progress = 0;
</script>

<style>
  .progress-container {
    margin: 20px 0;
    border: solid rgb(194, 194, 194) 1px;
  }

  .progress-bar {
    height: 30px;
    background: rgb(77, 199, 55);
    transition: all .2s ease-in;
  }

  .sr-only {
    display: none;
  }
</style>

<div class="progress-container">
  <div class="progress-bar" style="width: {progress}%;">
    <span class="sr-only">{progress}%</span>
  </div>
</div>
