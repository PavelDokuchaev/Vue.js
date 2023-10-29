<template>
  <div class="banner">
    <div class="banner-content">
      <h1 class="banner-content__title">Articles & News</h1>
      <p class="banner-content__text">Home / Blog</p>
    </div>
  </div>

  <div class="post center">
    <h1 class="post-title">Latest Post</h1>
    <div class="post-content">
      <img class="post-content__img" src="../assets/img/post.png" alt="post img">
      <div class="post-content__text">
        <h3 class="post-content__text-header">Low Cost Latest Invented Interior Designing Ideas</h3>
        <p class="post-content__text-desc">Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis dignissim
          maximus.posuere in.Contrary to popular belief.
          <br>
          Lorem Ipsum is not simply random text. It has roots in a piece of classica.
        </p>
        <div class="post-content__text-block">
          <p class="post-content__text-block_date">26 December,2022 </p>
          <button class="post-content__text-block_btn"><svg xmlns="http://www.w3.org/2000/svg" width="52" height="53"
              viewBox="0 0 52 53" fill="none">
              <circle cx="26" cy="26.5" r="26" fill="#F4F0EC" />
              <path d="M23.771 33.1855L29.7139 26.4998L23.771 19.8141" stroke="#292F36" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round" />
            </svg></button>
        </div>
      </div>
    </div>
  </div>

  <div class="articles center">
    <div class="articles-title">
      <h1 class="articles-title__head">Articles & News</h1>
    </div>
    <div id="app" class="articles-content">
      <div class="articles-content__item" v-for="item in articles" :key="item.id">
        <img class="articles-content__item-img" :src="item.img" alt="articles img">
        <div class="articles-content__item-subtitle">{{ item.rectangle }}</div>
        <h2 class="articles-content__item-title">
          {{ item.header }}
        </h2>
        <div class="articles-content__item-block">
          <p class="articles-content__item-block_text">{{ item.date }}</p>
          <button class="articles-content__item-block_btn"><router-link :to="{ name: 'BlogDetails' }"> <svg
                xmlns="http://www.w3.org/2000/svg" width="52" height="53" viewBox="0 0 52 53" fill="none">
                <circle cx="26" cy="26.267" r="26" fill="#F4F0EC" />
                <path d="M23.7714 32.9527L29.7143 26.267L23.7714 19.5813" stroke="#292F36" stroke-width="2"
                  stroke-linecap="round" stroke-linejoin="round" />
              </svg></router-link></button>
        </div>
      </div>
    </div>
  </div>

  <div class="pagination center">
    <button class="pagination-btn" type="button">01</button>
    <button class="pagination-btn" type="button">02</button>
    <button class="pagination-btn" type="button">03</button>
    <div class="pagination-img">
      <svg xmlns="http://www.w3.org/2000/svg" width="53" height="52" viewBox="0 0 53 52" fill="none">
        <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
        <path d="M23.5571 32L29.5 25.3143L23.5571 18.6286" stroke="#292F36" stroke-width="2" stroke-linecap="round"
          stroke-linejoin="round" />
      </svg>
    </div>
  </div>

  <FooterComponent />
</template>

<script>
import articles1 from "../assets/img/articles1.png";
import articles2 from "../assets/img/articles2.png";
import articles3 from "../assets/img/articles3.png";
import articles4 from "../assets/img/articles4.png";
import articles5 from "../assets/img/articles5.png";
import articles6 from "../assets/img/articles6.png";
import FooterComponent from "./FooterComponent.vue";

export default {
  data() {
    return {
      articles: [
        {
          id: 1, img: articles1, rectangle: "Kitchen Design", header: "Let’s Get Solution For Building Construction Work", date: "26 December,2022"
        },
        {
          id: 2, img: articles2, rectangle: "Living Design", header: "Low Cost Latest Invented Interior Designing Ideas.", date: "22 December,2022"
        },
        {
          id: 3, img: articles3, rectangle: "Interior Design", header: "Best For Any Office & Business Interior Solution", date: "25 December,2022"
        },
        {
          id: 4, img: articles4, rectangle: "Kitchen Design", header: "Let’s Get Solution For Building Construction Work", date: "26 December,2022"
        },
        {
          id: 5, img: articles5, rectangle: "Living Design", header: "Low Cost Latest Invented Interior Designing Ideas.", date: "22 December,2022"
        },
        {
          id: 6, img: articles6, rectangle: "Interior Design", header: "Best For Any Office & Business Interior Solution", date: "25 December,2022"
        },
      ],
    };
  },
  components: { FooterComponent }
}
</script>

<style lang="scss" scoped></style>