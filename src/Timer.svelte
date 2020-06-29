<script>
  import ProgressBar from "./ProgressBar.svelte";
</script>

<style>
  h2 {
    margin: 0;
  }

  button {
    outline: none;
    border: none;
    background: rgb(154, 73, 73) !important;
    color: #fff;
    width: 100%;
    margin: 10px 0;
    cursor: pointer;
  }
</style>

<h2>Seconds Left:</h2>
<ProgressBar />

<button>Start</button>
