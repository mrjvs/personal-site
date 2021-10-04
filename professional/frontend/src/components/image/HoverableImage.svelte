<script>
  export let src;
  export let alt = "";

  let styleUrl = "";
  $: styleUrl = `background-image: url('${src}')`;
</script>

<div class="hover-image-container">
  <div class="hover-image" role="img" aria-label={alt} style={styleUrl} />
</div>

<style lang="scss">
  @use 'colors' as c;

  .hover-image-container {
    height: 31rem;
    width: 25rem;
    display: flex;
    justify-content: center;
    align-items: center;

    &:hover .hover-image {
      filter: grayscale(0);
      height: 28rem;
      width: 24rem;
      transform: perspective(800px) translateZ(-8rem) rotateZ(-2deg)
        rotateY(0deg);
    }
  }

  .hover-image {
    width: 23rem;
    height: 25rem;
    background-position: center;
    background-size: cover;
    background-color: c.$bg_gray_200;
    filter: grayscale(1);
    transition: height 250ms ease-in-out, width 400ms ease-in-out,
      filter 250ms ease-in-out, transform 200ms ease-in-out;
    transform: perspective(800px) rotateY(-9deg);
    border-radius: 5px;
  }
</style>
