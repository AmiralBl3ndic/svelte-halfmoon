<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Button from "../../Button.svelte";
  import DarkModeWrapper from "../DarkModeWrapper.svelte";

  function logClicks(message) {
    return () => console.log(message);
  }
</script>

<Meta title="Svelte Halfmoon/Button/Variants" component={Button} />

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
  name="Primary"
  args={{
    content: "Primary button",
    variant: "primary",
  }}
/>

<Story
  name="Secondary"
  args={{
    content: "Secondary button",
    variant: "secondary",
  }}
/>

<Story
  name="Success"
  args={{
    content: "Success button",
    variant: "success",
  }}
/>

<Story
  name="Link"
  args={{
    content: "Link button",
    variant: "link",
  }}
/>

<Story
  name="Danger"
  args={{
    content: "Danger button",
    variant: "danger",
  }}
/>
