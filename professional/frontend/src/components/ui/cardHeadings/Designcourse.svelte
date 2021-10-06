<div class="wrapper">
  <div class="bg" />
  <div class="bg-overlay" />
  <img src="/images/designcourse-logo.svg" alt="Designcourse logo" />
</div>

<style lang="scss">
  .wrapper {
    width: 100%;
    height: 10rem;
    display: flex;
    position: relative;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;

    .bg,
    .bg-overlay {
      height: 12rem;
      width: 100%;
      position: absolute;
      z-index: 1;
      top: 0;
      left: 0;
      right: 0;
    }

    .bg {
      background-image: url("/images/dots.svg");
      background-size: cover;
      background-position: 0 -1rem;
      opacity: 0.8;
    }

    .bg-overlay {
      background: linear-gradient(
        to top,
        rgba(28, 30, 38, 1) 0%,
        rgba(28, 30, 38, 1) 15%,
        rgba(28, 30, 38, 0.2) 100%
      );
    }

    img {
      position: relative;
      width: 100%;
      max-width: 14rem;
      margin: 0 1rem;
      z-index: 5;
    }
  }
</style>
