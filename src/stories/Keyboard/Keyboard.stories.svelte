<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import DarkModeWrapper from "../DarkModeWrapper.svelte";
  import Keyboard from "../../components/Keyboard.svelte";
</script>

<Meta title="Svelte Halfmoon/Keyboard" component={Keyboard} />

<Template let:args>
  <DarkModeWrapper>
    <p>
      <Keyboard>{args.content}</Keyboard>
    </p>
  </DarkModeWrapper>
</Template>

<Story
  name="Keyboard"
  args={{
    content: "Cmd",
  }}
/>
