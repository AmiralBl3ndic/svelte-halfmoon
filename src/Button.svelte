<script lang="ts">
  import { createEventDispatcher } from "svelte";

  export let variant: ButtonVariant = "";
  export let large: boolean = false;
  export let small: boolean = false;
  export let block: boolean = false;
  export let darkMode: boolean = false;
  export let disabled: boolean = false;
  export let active: boolean = false;
  export let square: boolean = false;
  export let rounded: boolean = false;
  export let circle: boolean = false;

  const dispatch = createEventDispatcher();

  const onClick = (e: MouseEvent) => {
    dispatch("click", e);
  };

  const onDblClick = (e: MouseEvent) => {
    dispatch("dblclick", e);
  };

  const btnClasses = `btn${variant !== "" ? ` btn-${variant}` : ""}`;
</script>

<button
  type="button"
  class:dark-mode={darkMode}
  class={btnClasses}
  class:btn-lg={large}
  class:btn-sm={small}
  class:btn-block={block}
  class:btn-square={square}
  class:btn-rounded={rounded}
  class:rounded-circle={circle}
  class:disabled
  class:active
  {disabled}
  on:click={onClick}
  on:dblclick={onDblClick}
>
  <slot />
</button>
