
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Tour A-Frame</title>

<script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>

</head>

<body>



<a-scene inspector="" keyboard-shortcuts="" screenshot="" vr-mode-ui="" device-orientation-permission-ui="">

<a-entity camera="" position="" wasd-controls="" rotation="" look-controls="" aframe-injected=""></a-entity>

<div class="a-enter-vr" aframe-injected=""><button class="a-enter-vr-button" title="Enter VR mode with a headset or fullscreen mode on a desktop. Visit https://webvr.rocks or https://webvr.info for more information." aframe-injected=""></button></div>

<div class="a-enter-ar a-hidden" aframe-injected=""><button class="a-enter-ar-button" title="Enter AR mode with a headset or handheld device. Visit https://webvr.rocks or https://webvr.info for more information." aframe-injected=""></button></div>

<div class="a-orientation-modal a-hidden" aframe-injected=""><button aframe-injected="">Exit VR</button></div>

<a-entity light="" data-aframe-default-light="" aframe-injected=""></a-entity>

<a-entity light="color: #faebeb; intensity: 2; type: point"></a-entity>

<a-entity cursor="rayOrigin:mouse"></a-entity>



<script>
  AFRAME.registerComponent("weblink", {
    schema: {
      url: {
        default: ""
      }
    },
    init: function() {
      this.el.addEventListener("click", (e) => {
        window.location = this.data.url;
      })
    }
  })
</script>
  
  <!-- Ground -->

  <a-plane position="0.78094 -4.41441 7.80055" rotation="270 0 0" width="100" height="100" color="#8c8282" material="" geometry="" id="floor"></a-plane>

  <!-- Ceiling -->

  <a-plane position="0 34 9.75" rotation="90 0 0" width="100" height="100" color="#000000" material="" geometry="side: double" id="ceiling"></a-plane>  

    <a-entity geometry="primitive: cylinder; height: 50; segmentsHeight: 20; radius: 50" material="src: https://cdn.glitch.global/95edfa95-ed52-49f3-95ea-c84026a812a6/IMG_9566.jpg?v=1683818151427; color: #ada8a8; roughness: 1; side: double" position="-2.62931 11.09131 10">
  </a-entity>
  
  
  
<!-- Change position, text and weblink for each hotspot and photo. !-->
<!-- Duplicate a snippet below for additional hotspots, then customize them. -->
<!-- -->
<!-- BLOCK PLACEMENT -->
<!-- X is right positive, left negative  -->
<!-- Y is up negative, down negative  -->
<!-- Z is toward you positive, away from you negative  -->
<!-- -->
<!-- BLOCK ROTATION-->
<!-- X is tumbles toward or away from you.  -->
<!-- Y spins like a top.  -->
<!-- Z spins like a fan with blades facing you -->
<!-- -->

  <a-circle position="0, -2.6, 13" rotation="-70 180 0" width="20" height="20" radius="2" weblink="url:photo1.html">
    <a-entity geometry="primitive: circle; height: 2; segmentsHeight: 2; radius: 2" material="src: https://pachecod.github.io/aframepano/arrow.png; roughness: 1; side: double" position="0.025 -0.073 0.060">
    </a-entity>
  </a-circle>

  <a-circle position="0, -2.6, -13" rotation="60 180 0" width="20" height="20" radius="2" weblink="url:photo1.html">
    <a-entity geometry="primitive: circle; height: 2; segmentsHeight: 2; radius: 2" material="src: https://pachecod.github.io/aframepano/arrow.png; roughness: 1; side: double" position="0.025 -0.073 0.060">
    </a-entity>
  </a-circle>



</a-scene>


</body>
</html>
