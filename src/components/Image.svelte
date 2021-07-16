<script lang="ts">
  export let src: string;
  export let alt: string;

  export let rounded: boolean = false;
  export let roundedCircle: boolean = false;
  export let roundedTop: boolean = false;
  export let roundedBottom: boolean = false;
  export let roundedLeft: boolean = false;
  export let roundedRight: boolean = false;

  // https://www.gethalfmoon.com/static/site/img/image-1.png
</script>

<img
  {src}
  {alt}
  class="img-fluid"
  class:rounded
  class:rounded-circle={roundedCircle}
  class:rounded-top={roundedTop}
  class:rounded-bottom={roundedBottom}
  class:rounded-left={roundedLeft}
  class:rounded-right={roundedRight}
/>
