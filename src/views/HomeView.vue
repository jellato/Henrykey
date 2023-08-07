<template>
  <section class="home-section" id="home" v-motion-fade>
          <div class="container">
            <h2 class="section-heading">Hello Everyone!</h2>
            <IntroAnimation />
            <p class="section-text">
              My name is Wiley Haley, I'm a Full-Stack Developer based in Singapore. <br>
              I am working on web interfaces that should be good looking, simple and enjoyable to use.<br>
              If you are interested in cooperation and transforming your ideas into a great projects, please contact me in any way convenient for you.
            </p>
          </div>
        </section>
</template>

<script>
import IntroAnimation from '@/components/IntroAnimation.vue'

export default {
  name: 'HomeView',
  components: {
    IntroAnimation
  }
}
</script>

<style>
.home-section .section-heading {
	color: var(--home-color);
}
</style>
