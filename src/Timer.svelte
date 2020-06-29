<script>
  import { createEventDispatcher } from "svelte";
  import ProgressBar from "./ProgressBar.svelte";

  const totalSeconds = 20;
  let secondLeft = totalSeconds;
  let isRunning = false;
  $: progress = ((totalSeconds - secondLeft) / totalSeconds) * 100;

  const dispatch = createEventDispatcher();
  function startTimer() {
    const timer = setInterval(() => {
      secondLeft -= 1;
      isRunning = true;

      if (secondLeft == 0) {
        clearInterval(timer);
        isRunning = false;
        secondLeft = totalSeconds;
        dispatch("end", "end timer");
      }
    }, 1000);
  }
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
    padding: 10px 0;
    font-size: 18px;
    transition: all 0.2s ease;
  }
  button:disabled {
    background: #eee !important;
    cursor: not-allowed;
  }
</style>

<h2>Seconds Left: {secondLeft}</h2>
<ProgressBar {progress} />

<button on:click={startTimer} disabled={isRunning}>Start</button>
