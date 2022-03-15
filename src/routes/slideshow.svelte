<script lang="ts">

  import { onMount } from 'svelte';
      import { browser } from '$app/env';


var slideIndex = 1;
var slides;
var dots;
var i;

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
}

// Next/previous controls
function plusSlides(n) {
  showSlides(slideIndex += n);
console.log("browser is TRUE plusSlides");
}


if (browser){
plusSlides(2);
}

// Thumbnail image controls
function currentSlide(n) {
        if (browser){
  showSlides(slideIndex = n);
console.log("browser is TRUE currentSlide");
  } else {
console.log("browser is FALSE currentSlide");

}
}

onMount(async () => {
    showSlides(slideIndex);
});


</script>



<!-- Slideshow container -->


  <button class="prev bg-black " onclick="plusSlides(-1)">&#10094;</button>
  <button class="next bg-black " onclick="plusSlides(1)">&#10095;</button>
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div class="mySlides fade">
    <div class="numbertext">1 / 3</div>
    <img src="static/burg.jpg" alt="paul"  style="width:100%">
    <div class="text">paul</div>
  </div>

  <div class="mySlides fade">
    <div class="numbertext">2 / 3</div>
    <img src="static/paul.jpg" alt="burg" style="width:100%">
    <div class="text">burg</div>
  </div>

  <div class="mySlides fade">
    <div class="numbertext">3 / 3</div>
    <img src="static/postturm.jpg"  alt="postturm" style="width:100%">
    <div class="text">postturm</div>
  </div>

  <!-- Next and previous buttons -->
  <!--
  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>
  -->

  </div>
  
<br>

<!-- The dots/circles -->
<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span>
  <span class="dot" onclick="currentSlide(2)"></span>
  <span class="dot" onclick="currentSlide(3)"></span>
    <button class=" bg-gray-300 " onclick="showSlides(slideIndex)">showSlides</button>

</div>


  <button class="prev bg-black " onclick="plusSlides(-1)">&#10094;</button>
  <button class="next bg-black " onclick="plusSlides(1)">&#10095;</button>

