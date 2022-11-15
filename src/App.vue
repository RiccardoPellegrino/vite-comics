<template>
  <nav>
    <NavComponent />
  </nav>
  <div>
    <JumboComponent />
    <SectionComponent />
  </div>
  <div>
    <IconComponent />
  </div>
  <div>
    <DcComponent />
  </div>
  <footer>
    <FooterComponent />
  </footer>


</template>

<script>
import DcComponent from './components/DcComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import IconComponent from './components/IconComponent.vue';
import JumboComponent from './components/JumboComponent.vue';
import NavComponent from './components/NavComponent.vue';
import SectionComponent from './components/SectionComponent.vue';

export default {
  components: {
    NavComponent,
    SectionComponent,
    IconComponent,
    DcComponent,
    FooterComponent,
    JumboComponent
  }
}
</script>

<style lang="scss" scoped>

</style>