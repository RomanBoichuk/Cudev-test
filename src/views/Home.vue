<template>
  <div class="home">
    <Header/>
    <Content/>
    <Description/>
    <HowItWorks/>
    <MainSection/>
    <EndSection/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Content from '@/components/Content.vue'
import Description from '@/components/Description.vue'
import HowItWorks from '@/components/HowItWorks.vue'
import MainSection from '@/components/MainSection.vue'
import EndSection from '@/components/EndSection.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Content,
    Description,
    HowItWorks,
    MainSection,
    EndSection,
    Footer
  }
}
</script>

<style scoped lang="sass">
.home
  padding: 20px 0 20px 0
</style>
