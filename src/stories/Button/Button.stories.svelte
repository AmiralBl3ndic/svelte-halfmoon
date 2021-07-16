<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Button from "../../components/Button.svelte";
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
  name="Small"
  args={{
    content: "Small button",
    small: true,
  }}
/>

<Story
  name="Large"
  args={{
    content: "Large button",
    large: true,
  }}
/>

<Story
  name="Block"
  args={{
    content: "Block button",
    block: true,
  }}
/>

<Story
  name="Disabled"
  args={{
    content: "Disabled button",
    disabled: true,
  }}
/>

<Story
  name="Active"
  args={{
    content: "Active button",
    active: true,
  }}
/>

<Story
  name="Square"
  args={{
    content: "⬛️",
    square: true,
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
    content: "⭕️",
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
