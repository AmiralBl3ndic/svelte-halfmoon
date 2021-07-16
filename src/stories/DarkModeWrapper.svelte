<script>
  import Button from "../Button.svelte";

  function toggleDarkMode() {
    document.querySelector("body").classList.toggle("dark-mode");
  }
</script>

<div class="d-flex flex-row justify-content-between">
  <slot />

  <Button variant="link" on:click={toggleDarkMode}>Toggle dark mode</Button>
</div>
