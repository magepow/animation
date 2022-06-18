
## Docs

* [Animation](https://developer.mozilla.org/en-US/docs/Web/API/Animation/Animation)
* [Animate](https://developer.mozilla.org/en-US/docs/Web/API/Element/animate)
* [Animate interface](https://drafts.csswg.org/web-animations-1/#the-animation-interface)
* [Jquery animate](https://api.jquery.com/animate/)
* [Jquery animate VN](https://hocwebchuan.com/reference/jquery/jquery_animate.php)
* [Animate velocity](https://github.com/julianshapiro/velocity)
* [Animate gsap](https://greensock.com/jquerygsapjs/)
* [Css animate](https://animista.net/play/basic/shadow-drop)


```
// Web Animation API Keyframes options
var options = {
  iterations: Infinity,
  iterationStart: 0,
  delay: 0,
  endDelay: 0,
  direction: 'alternate',
  duration: 700,
  fill: 'forwards',
  easing: 'ease-out',
}
element.animate(keyframes, options);
```

```
https://codepen.io/rachelnabors/pen/eJyWzm/?editors=1000

var whiteRabbit = document.getElementById("rabbit");

var rabbitDownKeyframes = new KeyframeEffect(
    whiteRabbit, 
    [
      { transform: 'translateY(0%)' }, 
      { transform: 'translateY(100%)' }
    ], 
    { duration: 3000, fill: 'forwards' }
  );

var rabbitDownAnimation = new Animation(rabbitDownKeyframes, document.timeline);

// On tap or click,
whiteRabbit.addEventListener("mousedown", downHeGoes, false);
whiteRabbit.addEventListener("touchstart", downHeGoes, false);

// Trigger a single-fire animation
function downHeGoes(event) {

  // Remove those event listeners
  whiteRabbit.removeEventListener("mousedown", downHeGoes, false);
  whiteRabbit.removeEventListener("touchstart", downHeGoes, false);  

  // Play rabbit animation
  rabbitDownAnimation.play();
    
}
```