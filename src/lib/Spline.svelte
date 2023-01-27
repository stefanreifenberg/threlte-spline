<script>
import SplineLoader from '@splinetool/loader';
import { Three, OrbitControls } from '@threlte/core'
import { PerspectiveCamera } from 'three'

// Instantiate a loader
const loader = new SplineLoader();
// define a model variable
let model;
// load the spline scene
loader.load(
    'https://prod.spline.design/bPyo53wTrYqJgajV/scene.splinecode',
    (splineScene) => {
    model = splineScene;
});
</script>

<!-- Camera Setup -->
<Three type={PerspectiveCamera} makeDefault position={[500, 500, 500]} fov={60} near={1} far={5000} >
    <OrbitControls autoRotate target={{ y: 0.5 }} />
</Three>

<!-- Render the spline scene -->
{#if model}
    <Three type={model} scale={0.3} />
{/if}