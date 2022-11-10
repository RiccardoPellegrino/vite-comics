<template>
  <nav>
    <NavComponent />
  </nav>
  <div>
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
import NavComponent from './components/NavComponent.vue';
import SectionComponent from './components/SectionComponent.vue';

export default {
  components: { NavComponent, SectionComponent, IconComponent, DcComponent, FooterComponent }
}
</script>

<style lang="scss" scoped>

</style>