[slide]
# JQuery Modal

```
<!-- Remember to include jQuery :) -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.0.0/jquery.min.js"></script>

<!-- jQuery Modal -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-modal/0.9.1/jquery.modal.min.js"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jquery-modal/0.9.1/jquery.modal.min.css" />
```

[html]
<style>
p.custom-p {
  color: black;
}
</style>

 <!-- Remember to include jQuery :) -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.0.0/jquery.min.js"></script>

    <!-- jQuery Modal -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-modal/0.9.1/jquery.modal.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jquery-modal/0.9.1/jquery.modal.min.css" />
    
        <script type="text/javascript" charset="utf-8">
        $(function () {
            $('a[href="#fademodal"]').click(function (event) {
                event.preventDefault();
                $(this).modal({
                    fadeDuration: 250
                });
            });

            $('a[href="#fademodaldelayed"]').click(function (event) {
                event.preventDefault();
                $(this).modal({
                    fadeDuration: 1000,
                    fadeDelay: 0.50
                });
            });

        });
    </script>
    
 <!-- Modal HTML embedded directly into document -->
    <div id="fademodal" class="modal">
        <p class="custom-p">That was some smooth fade effect. I like it a lot!</p>
        <a href="#" rel="modal:close">Close</a>
    </div>

    <!-- Link to open the modal -->
    <p><a href="#fademodal">Open Modal</a></p>



[/html]

[/slide]

[slide]
# Anime JS
[html]
<style>
  h1.ml8 {
  font-weight: 900;
  font-size: 4.5em;
  color: #fff;
  width: 3em;
  height: 3em;
}

.ml8 .letters-container {
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
  top: 0;
  bottom: 0;
  height: 1em;
  text-align: center;
}

.ml8 .letters {
  position: relative;
  z-index: 2;
  display: inline-block;
  line-height: 0.7em;
  right: -0.12em;
  top: -0.2em;
}

.ml8 .bang {
  font-size: 1.4em;
  top: auto;
  left: -0.06em;
}

.ml8 .circle {
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
  top: 0;
  bottom: 0;
}

.ml8 .circle-white {
  width: 3em;
  height: 3em;
  border: 2px dashed white;
  border-radius: 2em;
}

.ml8 .circle-dark {
  width: 2.2em;
  height: 2.2em;
  background-color: #4f7b86;
  border-radius: 3em;
  z-index: 1;
}

.ml8 .circle-dark-dashed {
  border-radius: 2.4em;
  background-color: transparent;
  border: 2px dashed #4f7b86;
  width: 2.3em;
  height: 2.3em;
}
</style>

<script>
  anime.timeline({loop: true})
  .add({
    targets: '.ml8 .circle-white',
    scale: [0, 3],
    opacity: [1, 0],
    easing: "easeInOutExpo",
    rotateZ: 360,
    duration: 1100
  }).add({
    targets: '.ml8 .circle-container',
    scale: [0, 1],
    duration: 1100,
    easing: "easeInOutExpo",
    offset: '-=1000'
  }).add({
    targets: '.ml8 .circle-dark',
    scale: [0, 1],
    duration: 1100,
    easing: "easeOutExpo",
    offset: '-=600'
  }).add({
    targets: '.ml8 .letters-left',
    scale: [0, 1],
    duration: 1200,
    offset: '-=550'
  }).add({
    targets: '.ml8 .bang',
    scale: [0, 1],
    rotateZ: [45, 15],
    duration: 1200,
    offset: '-=1000'
  }).add({
    targets: '.ml8',
    opacity: 0,
    duration: 1000,
    easing: "easeOutExpo",
    delay: 1400
  });

anime({
  targets: '.ml8 .circle-dark-dashed',
  rotateZ: 360,
  duration: 8000,
  easing: "linear",
  loop: true
});
</script>

<h1 class="ml8">
  <span class="letters-container">
    <span class="letters letters-left">Hi</span>
    <span class="letters bang">!</span>
  </span>
  <span class="circle circle-white"></span>
  <span class="circle circle-dark"></span>
  <span class="circle circle-container"><span class="circle circle-dark-dashed"></span></span>
</h1>

<script src="https://cdnjs.cloudflare.com/ajax/libs/animejs/2.0.2/anime.min.js"></script>
[/html]
[/slide]
