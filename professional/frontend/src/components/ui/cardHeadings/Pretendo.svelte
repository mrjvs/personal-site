<div class="wrapper">
  <div class="gradient" />
  <img src="/images/pretendo-logo.svg" alt="pretendo logo" />
</div>

<style lang="scss">
  .wrapper {
    width: 100%;
    height: 8rem;
    padding-top: 2rem;
    display: flex;
    position: relative;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;

    .gradient {
      background-color: #383258;
      background: linear-gradient(
        to bottom,
        rgba(56, 50, 88, 1),
        rgba(56, 50, 88, 0)
      );
      height: 150%;
      position: absolute;
      z-index: 1;
      top: 0;
      left: 0;
      right: 0;
      width: 100%;
      opacity: 0.67;
    }

    img {
      position: relative;
      width: 100%;
      max-width: 11rem;
      margin: 0 1rem;
      z-index: 5;
    }
  }
</style>
