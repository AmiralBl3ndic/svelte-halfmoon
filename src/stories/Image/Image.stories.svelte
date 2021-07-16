<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import DarkModeWrapper from "../DarkModeWrapper.svelte";
  import Image from "../../components/Image.svelte";

  const src = "https://www.gethalfmoon.com/static/site/img/image-2.png";
  const alt = "Plaholder image";
</script>

<Meta title="Svelte Halfmoon/Image" component={Image} />

<Template let:args>
  <DarkModeWrapper>
    <Image {...args} />
  </DarkModeWrapper>
</Template>

<Story
  name="Default"
  args={{
    src,
    alt,
  }}
/>

<Story
  name="Rounded"
  args={{
    src,
    alt,
    rounded: true,
  }}
/>

<Story
  name="Rounded top"
  args={{
    src,
    alt,
    roundedTop: true,
  }}
/>

<Story
  name="Rounded bottom"
  args={{
    src,
    alt,
    roundedBottom: true,
  }}
/>

<Story
  name="Rounded left"
  args={{
    src,
    alt,
    roundedLeft: true,
  }}
/>

<Story
  name="Rounded right"
  args={{
    src,
    alt,
    roundedRight: true,
  }}
/>
