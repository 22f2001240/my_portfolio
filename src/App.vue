<template>
  <div class="bg-[#111827] min-h-screen">
    <!--Wrap compo. in suspense to handle loading-->
    <Suspense>
      <template #default>
        <div>
          <NavBar />
          <HeroSection />
          <ServiceSection />
          <AboutSection />
          <ExperienceAndSkills />
          <Projects />
          <ContactSection />
          <Footer />
          <BackToTop />
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
  </div>
</template>

<script setup>
import {defineAsyncComponent} from 'vue'
 // import components Asynchronously
const NavBar = defineAsyncComponent(() => import('@/components/NavBar.vue'))
const HeroSection = defineAsyncComponent(() => import('@/components/HeroSection.vue'))
const ServiceSection = defineAsyncComponent(() => import('@/components/ServiceSection.vue'))
const AboutSection = defineAsyncComponent(() => import('@/components/AboutSection.vue'))
const ExperienceAndSkills = defineAsyncComponent(() => import('@/components/ExperienceAndSkills.vue'))  
const Projects = defineAsyncComponent(() => import('@/components/Projects.vue'))
const ContactSection = defineAsyncComponent(() => import('@/components/ContactSection.vue'))
const Footer = defineAsyncComponent(() => import('@/components/Footer.vue'))
const BackToTop = defineAsyncComponent(() => import('@/components/BackToTop.vue'))
import LoadingSpinner from '@/components/LoadingSpinner.vue'
</script>

<style>

*{
  scrollbar-width: thin;
  scrollbar-color: #111827 #f1f1f1;
}
</style>