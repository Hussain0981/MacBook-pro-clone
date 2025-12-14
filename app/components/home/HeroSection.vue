<template>
  <section class="xl:pt-38 h-screen min-w-full flex flex-col items-center justify-center text-center px-4 gap-5">
    <!-- Title -->
    <div>
      <h1 class="text-3xl sm:text-4xl md:text-5xl font-semibold tracking-wide text-white/80">
        Probook Menu
      </h1>
      <img class="w-full sm:w-1/2 mx-auto mt-2" src="/title.png" alt="ProBook" />
    </div>

    <!-- Video -->
    <div class="w-full col-center xl:relative xl:-translate-y-8">
      <video class="w-full max-w-4xl  sm:w-4/5 rounded-xl shadow-lg" muted ref="videoRef"
        autoplay playsinline src="/videos/hero.mp4" />
      <div>
        <!-- CTA -->
        <button class=" cursor-pointer px-4 py-2 rounded-full bg-blue-500 text-white font-medium
      hover:bg-white hover:text-black 
      transition-all duration-200">
          Buy
        </button>

        <!-- Description -->
        <p class="max-w-md mt-2 text-sm sm:text-base text-gray-400">
          From $1599.00 or $66.62/mo. for 24 mo. Footnote*
        </p>
      </div>
    </div>


  </section>
</template>

<script setup lang="ts">
const videoRef = ref<HTMLVideoElement | null>(null)

onMounted(() => {

  const video = videoRef.value
  if (!video) return
  if (videoRef.value) {
    videoRef.value.playbackRate = 2
  }
})
</script>

<style scoped>
/* reserved for future custom animations */
</style>
