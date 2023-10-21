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
</template>

<script>
import IndexComponent from './components/IndexComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import ArticlesComponent from './components/ArticlesComponent.vue';
import BlogDetailsComponent from './components/BlogDetailsComponent.vue';

export default {
  components: {
    IndexComponent,
    HeaderComponent,
    FooterComponent,
    ArticlesComponent,
    BlogDetailsComponent
  }
};
</script>

<style lang="scss"></style>
