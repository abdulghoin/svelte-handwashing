<script>
  import Timer from "./Timer.svelte";
  import HowTo from "./HowTo.svelte";

  let audio;

  function timerEnds() {
    audio.play();
  }
</script>

<style>
  h1,
  h3 {
    text-align: center;
  }
</style>

<div bp="grid">
  <div bp="offset-5@md 4@md 12@sm">
    <h1>Handwashing App</h1>
    <Timer on:end={timerEnds} />
    <HowTo />

    <h3>
      <a
        href="https://www.who.int/gpsc/clean_hands_protection/en/"
        target="_blank">
        Picture source
      </a>
    </h3>
    <h3>
      <a
        href="https://www.who.int/gpsc/clean_hands_protection/en/"
        target="_blank">
        Sound source
      </a>
    </h3>
  </div>
</div>
<audio bind:this={audio}>
  <source src="sound.wav" />
</audio>
