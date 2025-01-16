<template>
  <div class="flex items-center justify-center h-screen w-full">
    <img id="img" class="w-64 h-64" src="~/assets/images/img.webp" alt="" />
  </div>
</template>

<script setup lang="ts">
import gsap from "gsap";

function tween(
  duration: number,
  delay: number,
  rotate: number,
  skew: number,
  ease: string
) {
  gsap.to("#img", {
    duration: duration,
    delay: delay,
    rotate: rotate,
    skew: skew,
    ease: ease,
  });
}

onMounted(async () => {
    tween(3,1,2880,45,"power1.in")
});
</script>
