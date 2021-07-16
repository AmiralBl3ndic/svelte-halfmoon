<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import DarkModeWrapper from "../DarkModeWrapper.svelte";
  import Code from "../../components/Code.svelte";
</script>

<Meta title="Svelte Halfmoon/Code" component={Code} />

<Template let:args>
  <DarkModeWrapper>
    <p>
      <Code>{args.content}</Code>
    </p>
  </DarkModeWrapper>
</Template>

<Story
  name="Code"
  args={{
    content: 'console.log("Hello, world")',
  }}
/>
