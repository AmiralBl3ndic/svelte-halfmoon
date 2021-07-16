<script lang="ts">
  import { createEventDispatcher } from "svelte";

  /**
   * Color variant of the button
   */
  export let variant: ButtonVariant = "";

  /**
   * Use the `btn-lg` variant of the button
   */
  export let large: boolean = false;

  /**
   * Use the `btn-sm` variant of the button
   */
  export let small: boolean = false;

  /**
   * Use the `btn-block` variant of the button
   */
  export let block: boolean = false;

  /**
   * Disable the button
   */
  export let disabled: boolean = false;

  /**
   * Mark the button as active
   */
  export let active: boolean = false;

  /**
   * Make the button a square
   */
  export let square: boolean = false;

  /**
   * Round corners of the button
   */
  export let rounded: boolean = false;

  /**
   * Make the button a circle
   */
  export let circle: boolean = false;

  const dispatch = createEventDispatcher();

  const onClick = (e: MouseEvent) => {
    dispatch("click", e);
  };

  const onDblClick = (e: MouseEvent) => {
    dispatch("dblclick", e);
  };

  if (circle) {
    square = true;
  }

  const btnClasses = `btn${variant !== "" ? ` btn-${variant}` : ""}`;
</script>

<button
  type="button"
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
