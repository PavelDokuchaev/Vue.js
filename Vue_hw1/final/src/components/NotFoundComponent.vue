<template>
  <div class="pagenotfound">
    <div class="pagenotfound-content">
      <h1 class="pagenotfound-content__header">404</h1>
      <p class="pagenotfound-content__text">We are sorry, but the page
        you requested was not found</p>
      <button class="pagenotfound-content__button"><router-link class="button-link" :to="link.url">Back To Home <svg
            width="19" height="17" viewBox="0 0 19 17" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M2 8.43542L15.7232 8.29857M10.6182 1.91138L17.1412 8.43436L10.4868 15.0887" stroke="#CDA274"
              stroke-width="2" stroke-linecap="square" stroke-linejoin="round" />
          </svg></router-link>
      </button>
    </div>
    <img src="../assets/img/pagenotfound.png" alt="not found page">
  </div>
</template>

<script>
export default {
  data() {
    return {
      link: {
        name: 'Home',
        url: '/'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.pagenotfound {
  display: flex;
  gap: 81px;
  padding-left: calc(50% - 600px);

  &-content {
    padding-top: 309px;
    padding-bottom: 309px;

    &__header {
      font-family: 'DM Serif Display';
      font-size: 250px;
      color: #CDA274;
      margin-bottom: 20px;
    }

    &__text {
      font-family: 'DM Serif Display';
      font-size: 35px;
      margin-bottom: 20px;
    }

    &__button {
      border-radius: 18px;
      border: none;
      padding: 26px 49px 26px 48px;
      background-color: #292F36;

      .button-link {
        color: #fff;
        font-family: 'Jost';
        font-size: 18px;
        display: flex;
        gap: 10px;
        align-items: center;
      }
    }

    &__button:hover {
      background-color: #4D5053;
      cursor: pointer;
    }
  }
}
</style>