<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Button from "../../Button.svelte";
  import DarkModeWrapper from "../DarkModeWrapper.svelte";

  function logClicks(message) {
    return () => console.log(message);
  }
</script>

<Meta title="Svelte Halfmoon/Button" component={Button} />

<Template let:args>
  <DarkModeWrapper>
    <Button
      {...args}
      on:click={args.onClick || logClicks("single click")}
      on:dblclick={args.onDblclick || logClicks("double click")}
      >{args.content}</Button
    >
  </DarkModeWrapper>
</Template>

<Story
  name="Default"
  args={{
    content: "Default button",
  }}
/>

<Story
  name="Rounded"
  args={{
    content: "Rounded button",
    rounded: true,
  }}
/>

<Story
  name="Circle"
  args={{
    content: "🚀",
    circle: true,
  }}
/>

<Story
  name="Rounded"
  args={{
    content: "Rounded button",
    rounded: true,
  }}
/>
