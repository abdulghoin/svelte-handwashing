<script>
  import Timer from "./Timer.svelte";
  import HowTo from "./HowTo.svelte";
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
    <Timer />
    <HowTo />

    <h3>
      <a href="https://www.who.int/gpsc/clean_hands_protection/en/">
        Picture source
      </a>
    </h3>
    <h3>
      <a href="https://www.who.int/gpsc/clean_hands_protection/en/">
        Sound source
      </a>
    </h3>
  </div>
</div>
