# deutschlernmaterialien
<div id="custom-animation-container">
<style>
body {
  background-color: black;
  height:100vh;
  width:100vw;
  overflow-y:hidden;
  overflow-x:hidden;
}
.petal {
  width: 1rem;
  height: 1rem;
  display: inline-block;
  position: absolute;
  top: -10rem;
  bottom:0;
  z-index: 150;
}
.petal .rotate {
  animation: driftyRotate 1s infinite both ease-in-out;
  perspective: 1000;
}
.petal .askew {
  background: currentColor;
  transform: skewY(10deg);
  display: block;
  width: 2rem;
  height: 2rem;
  animation: drifty 1s infinite alternate both ease-in-out;
  perspective:1000;
}

.petal {
  color: rgba(0,0,0,0);
}
.petal:nth-of-type(7n) .askew {
  animation-delay: -.6s;
  animation-duration: 2.25s;
}
.petal:nth-of-type(7n + 1) .askew {
  animation-delay: -.879s;
  animation-duration: 3.5s;
}
.petal:nth-of-type(7n + 2) .askew {
  animation-delay: -.11s;
  animation-duration: 1.95s;
}
.petal:nth-of-type(7n + 3) .askew {
  animation-delay: -.246s;
  animation-duration: .85s;
}
.petal:nth-of-type(7n + 4) .askew {
  animation-delay: -.43s;
  animation-duration: 2.5s;
}
.petal:nth-of-type(7n + 5) .askew {
  animation-delay: -.56s;
  animation-duration: 1.75s;
}
.petal:nth-of-type(7n + 6) .askew {
  animation-delay: -.76s;
  animation-duration: 1.5s;
}
  
.petal:nth-of-type(9n) .rotate {
  animation-duration: 2s;
}
.petal:nth-of-type(9n + 1) .rotate {
  animation-duration: 2.3s;
}
.petal:nth-of-type(9n + 2) .rotate {
  animation-duration: 1.1s;
}
.petal:nth-of-type(9n + 3) .rotate {
  animation-duration: .75s;
}
.petal:nth-of-type(9n + 4) .rotate {
  animation-duration: 4.3s;
}
.petal:nth-of-type(9n + 5) .rotate {
  animation-duration: 3.05s;
}
.petal:nth-of-type(9n + 6) .rotate {
  animation-duration: 2.76s;
}
.petal:nth-of-type(9n + 7) .rotate {
  animation-duration: 7.6s;
}
.petal:nth-of-type(9n + 8) .rotate {
  animation-duration: 1.78s;
}

@keyframes drifty {
  0% {
    transform: skewY(10deg) translate3d(-250%, 0, 0);
    display:block;
  }
  100% {
    transform: skewY(-12deg) translate3d(250%, 0, 0);
    display:block;
  }
}
@keyframes driftyRotate {
  0% {
    transform: rotateX(0);
    display:block;
  }
  100% {
    transform: rotateX(359deg);
    display:block;
  }
}
</style>
<body>
<div id="petals-container">
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
</div>

<script>
var petalPlayers = [];

function animatePetals() {
  var petals = document.querySelectorAll('.petal');
  
  if (!petals[0].animate) {
    var petalsContainer = document.getElementById('petals-container');
    petalsContainer.prepend("Uh oh, it seems like your browser doesn't support Web Animations API yet. Have you tried this in Firefox or Chrome?");
    return false;
  }

  for (var i = 0, len = petals.length; i < len; ++i) {
    var petal = petals[i];
    petal.innerHTML = '<div class="rotate"><img src="https://qqz.works/wp-content/uploads/2021/08/petal.png" class="askew"></div>';
    var scale = Math.random() * .8 + .2;


    var player = petal.animate([
      { transform: 'translate3d(' + (i/len*100) + 'vw,0,0) scale(' + scale + ')', opacity: scale },
      { transform: 'translate3d(' + (i/len*100 + 10) + 'vw,150vh,0) scale(' + scale + ')', opacity: 1 }
    ], {
      duration: Math.random() * 90000 + 3000,
      iterations: Infinity,
      delay: -(Math.random() * 5000)
    });
    
    petalPlayers.push(player);
  }
}

function initAnimation() {
  requestAnimationFrame(animatePetals);
}

window.onload = initAnimation;

</script>
</body>
</div>
