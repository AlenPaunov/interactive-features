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

<!-- Modal HTML embedded directly into document -->
<div id="ex1" class="modal">
  <p class="custom-p">Thanks for clicking. That felt good.</p>
  <a href="#" rel="modal:close">Close</a>
</div>

<!-- Link to open the modal -->
<p><a href="#ex1" rel="modal:open">Open Modal</a></p>

<!-- Modal HTML embedded directly into document -->
<div id="fademodal" class="">
<p>That was some smooth fade effect. I like it a lot!</p>
<a href="#" rel="modal:close">Close</a>
</div>

<!-- Link to open the modal -->
<p><a href="#fademodal">Open Modal</a></p>

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


[/html]

[/slide]
