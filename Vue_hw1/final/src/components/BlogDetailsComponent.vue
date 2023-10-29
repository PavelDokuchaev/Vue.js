<template>
  <div class="bannerblog">
  </div>

  <div id="app" class="blog center">
    <component :is="changeTabs"></component>
    <div class="blog-tags">
      <button class="blog-tags__btn" @click="currentTab = 'KitchenComponent'">Kitchen</button>
      <button class="blog-tags__btn" @click="currentTab = 'BedroomComponent'">Bedroom</button>
      <button class="blog-tags__btn" @click="currentTab = 'BuildingComponent'">Building</button>
      <button class="blog-tags__btn" @click="currentTab = 'ArchitectureComponent'">Architecture</button>
      <button class="blog-tags__btn" @click="currentTab = 'KitchenPlanningComponent'">Kitchen planning</button>
      <button class="blog-tags__btn" @click="currentTab = 'BedroomComponent'">Bedroom</button>
    </div>
  </div>

  <FooterComponent />
</template>

<script>
import Change_ArchitectureComponent from './Change_ArchitectureComponent.vue';
import Change_BedroomComponent from './Change_BedroomComponent.vue';
import Change_BuildingComponent from './Change_BuildingComponent.vue';
import Change_KitchenComponent from './Change_KitchenComponent.vue';
import Change_KitchenPlanningComponent from './Change_KitchenPlanningComponent.vue';
import FooterComponent from './FooterComponent.vue';

export default {
  data() {
    return {
      currentTab: 'KitchenComponent',
    }
  },

  computed: {
    changeTabs() {
      return `Change_${this.currentTab}`;
    }
  },

  components: { Change_KitchenComponent, Change_BedroomComponent, Change_BuildingComponent, Change_ArchitectureComponent, Change_KitchenPlanningComponent, FooterComponent }
}
</script>

<style lang="scss" scoped></style>