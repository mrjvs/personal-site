<div class="wrapper">
  <div class="circle" />
  <img src="/images/amboats-logo.svg" alt="Amsterdam Boats Tickets logo" />
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
    margin-bottom: 1rem;

    .circle {
      background-color: #181920;
      height: 30rem;
      width: 80rem;
      position: absolute;
      z-index: 1;
      top: -20rem;
      left: 50%;
      transform: translateX(-50%);
      right: 0;
      border-radius: 50%;
    }

    img {
      position: relative;
      width: 100%;
      max-width: 22rem;
      margin: 0 1rem;
      z-index: 5;
    }
  }
</style>
