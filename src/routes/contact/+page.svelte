<script>
    import { slide } from "svelte/transition";
import PageHeader from "../../lib/components/PageHeader.svelte";

// Carousel

const slideArr = [1, 2, 3, 4, 5];
let currentSlideContent = slideArr[0];
// Current index counter
let currentSlide = 0;
//  max length of array
const maxLength = slideArr.length - 1;

// next function
function nextSlide() {
  if (currentSlide === maxLength){
    currentSlide = 0;
    currentSlideContent = slideArr[currentSlide];
  } else {
    currentSlide ++;
    currentSlideContent = slideArr[currentSlide];
  }
};

// prev function
function prevSlide() {
   if (currentSlide === 0){
    currentSlide = maxLength;
    currentSlideContent = slideArr[currentSlide];
  } else {
    currentSlide --;
    currentSlideContent = slideArr[currentSlide];
  }
};
</script>
<PageHeader />
<h2 class="text-3xl">Basic Carousel</h2>
<!-- Carousel -->
<h2 class="text-2xl">{currentSlide}</h2>
<button on:click={prevSlide}>prev</button>
<button on:click={nextSlide}>next</button>
