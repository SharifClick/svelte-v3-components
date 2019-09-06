<script>
  import Swipe from "svelte-swipe";
  let play_slider = false;
  let play_delay = 1000;
  
  function toggle(){
    play_slider = !play_slider;
  }

</script>

<style>
  :root{
    --sv-swipe-panel-height: 90%;
    /* --sv-swipe-indicator-active-color:grey; */
  }
  .is-center{
    display: flex;
    justify-content: center;
    border: 1px solid green;
    position: absolute;
    width: 99%;
  }
</style>

<Swipe showIndicators={true} autoplay={play_slider} delay={play_delay}>
  <div class="swipeable-item is-center">
    <img src="https://source.unsplash.com/user/erondu/1600x900" alt="">
  </div>

  <div class="swipeable-item is-center">
    <img src="https://source.unsplash.com/user/erondu/1600x900" alt="">
  </div>

  <div class="swipeable-item is-center">
    <img src="https://source.unsplash.com/user/erondu/1600x900" alt="">
  </div>

  <div class="swipeable-item is-center">
    <img src="https://source.unsplash.com/user/erondu/1600x900" alt="">
  </div>
</Swipe>

<div style="margin-top: 100px">
  <button on:click={toggle} >{play_slider ? 'Stop': 'Play'}</button>
  <input type="text" bind:value={play_delay} />
</div>
