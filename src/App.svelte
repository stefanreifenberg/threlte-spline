<script>
  import { Canvas} from '@threlte/core'
  import Scene from './lib/Scene.svelte';
  import Spline from './lib/Spline.svelte';

</script>


<div class="canvas-wrapper">
	<Canvas>
    <Spline />
	</Canvas>
</div>


<div class="hero">
  <section class="">
      <div class="big-text">
          <div >
              <h1>Threlte &#128156; Spline</h1>
          </div>
      </div>
  </section>
</div>

<style>
 .canvas-wrapper {
    position: sticky;
    top: 0;
    width: 100vw;
    height: 100vh;
  }

  .hero {
    height: 30%;
    font-family: 'West', sans-serif;
    font-size: 1.5rem;
    position: absolute;
    width: 100%;
    margin: auto;
    margin-bottom: 12rem;
    display: flex;
    place-items: center;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    z-index: 2;
    top: 0;
}

</style>