<template>
  <HeaderComponent />
  <IndexComponent />
  <FooterComponent />
  <HeaderComponent />
  <ArticlesComponent />
  <FooterComponent />
  <HeaderComponent />
  <BlogDetailsComponent />
  <FooterComponent />
  <HeaderComponent />
  <ProjectComponenet />
  <FooterComponent />
</template>

<script>
import IndexComponent from './components/IndexComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import ArticlesComponent from './components/ArticlesComponent.vue';
import BlogDetailsComponent from './components/BlogDetailsComponent.vue';
import ProjectComponenet from './components/ProjectComponenet.vue';

export default {
  components: {
    IndexComponent,
    HeaderComponent,
    FooterComponent,
    ArticlesComponent,
    BlogDetailsComponent,
    ProjectComponenet
  }
};
</script>

<style lang="scss"></style>
