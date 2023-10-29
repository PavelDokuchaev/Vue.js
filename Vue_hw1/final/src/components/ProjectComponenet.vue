<template>
  <div class="banner">
    <div class="banner-content">
      <h1 class="banner-content__title">Our Project</h1>
      <p class="banner-content__text">Home / Project</p>
    </div>
  </div>

  <div class="project">
    <div class="project-buttons">
      <button class="project-buttons__item" @click="getProject('bathroom')">Bathroom</button>
      <button class="project-buttons__item" @click="getProject('bedroom')">Bedroom</button>
      <button class="project-buttons__item" @click="getProject('kitchen')">Kitchen</button>
      <button class="project-buttons__item" @click="getProject('living')">Living Area</button>
    </div>

    <div class="project-content">
      <div class="project-content__item" v-for="project in temp" :key="project.id">
        <img class="project-content__item-img" :src="project.img" alt="">
        <svg class="project-content__item-star" @click="addFavourite" xmlns="http://www.w3.org/2000/svg" width="36"
          height="35" viewBox="0 0 36 35" fill="none">
          <g filter="url(#filter0_d_993_156)">
            <path
              d="M16.0992 1.80951C16.7004 -0.0279021 19.2996 -0.0279021 19.9008 1.80951L21.7983 7.60879C22.0673 8.43084 22.8342 8.98685 23.6992 8.98685H29.8097C31.7506 8.98685 32.5539 11.4732 30.98 12.6088L26.0604 16.1581C25.3546 16.6674 25.0591 17.5748 25.3298 18.402L27.2146 24.1623C27.8166 26.0025 25.7137 27.539 24.1435 26.4062L19.1702 22.818C18.4715 22.3139 17.5285 22.3139 16.8298 22.818L11.8565 26.4062C10.2863 27.539 8.18335 26.0025 8.78545 24.1623L10.6702 18.402C10.9409 17.5748 10.6454 16.6674 9.93955 16.1581L5.02004 12.6088C3.44611 11.4732 4.24942 8.98685 6.19025 8.98685H12.3008C13.1658 8.98685 13.9327 8.43084 14.2017 7.60879L16.0992 1.80951Z"
              fill="#FFA928" />
          </g>
          <defs>
            <filter id="filter0_d_993_156" x="0.186424" y="0.431396" width="35.6271" height="34.3619"
              filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
              <feFlood flood-opacity="0" result="BackgroundImageFix" />
              <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                result="hardAlpha" />
              <feOffset dy="4" />
              <feGaussianBlur stdDeviation="2" />
              <feComposite in2="hardAlpha" operator="out" />
              <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
              <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_993_156" />
              <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_993_156" result="shape" />
            </filter>
          </defs>
        </svg>

        <div class="project-content__item-textblock">
          <div class="project-content__item-textblock_item">
            <h3 class="project-content__item-textblock_item-title">{{ project.header }}</h3>
            <p class="project-content__item-textblock_item-text">{{ project.text }}</p>
          </div>
          <router-link :to="{ name: 'ProjectDetails' }">
            <svg width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="35" cy="35" r="35" fill="#F4F0EC" />
              <path d="M32 44L40 35L32 26" stroke="#292F36" stroke-width="2" stroke-linecap="round"
                stroke-linejoin="round" />
            </svg>
          </router-link>
        </div>
      </div>
    </div>

    <div class="pagination">
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
  </div>

  <FooterComponent />
</template>

<script>
import bedroomProj1 from '../assets/img/bedroomProj1.png';
import bedroomProj2 from '../assets/img/bedroomProj2.png';
import bedroomProj3 from '../assets/img/bedroomProj3.png';
import bedroomProj4 from '../assets/img/bedroomProj4.png';
import bedroomProj5 from '../assets/img/bedroomProj5.png';
import bedroomProj6 from '../assets/img/bedroomProj6.png';
import bedroomProj7 from '../assets/img/bedroomProj7.png';
import bedroomProj8 from '../assets/img/bedroomProj8.png';
import bathroom1 from '../assets/img/bathroom1.jpg';
import bathroom2 from '../assets/img/bathroom2.jpeg';
import bathroom3 from '../assets/img/bathroom3.jpg';
import bathroom4 from '../assets/img/bathroom4.jpg';
import bathroom5 from '../assets/img/bathroom5.jpg';
import bathroom6 from '../assets/img/bathroom6.jpg';
import bathroom7 from '../assets/img/bathroom7.jpg';
import bathroom8 from '../assets/img/bathroom8.jpg';
import kitchan1 from '../assets/img/kitchan1.jpg';
import kitchan2 from '../assets/img/kitchan2.jpg';
import kitchan3 from '../assets/img/kitchan3.jpg';
import kitchan4 from '../assets/img/kitchan4.jpg';
import kitchan5 from '../assets/img/kitchan5.jpg';
import kitchan6 from '../assets/img/kitchan6.jpg';
import kitchan7 from '../assets/img/kitchan7.jpg';
import kitchan8 from '../assets/img/kitchan8.jpg';
import livingarea1 from '../assets/img/livingarea1.jpg';
import livingarea2 from '../assets/img/livingarea2.jpg';
import livingarea3 from '../assets/img/livingarea3.jpg';
import livingarea4 from '../assets/img/livingarea4.jpeg';
import livingarea5 from '../assets/img/livingarea5.jpg';
import livingarea6 from '../assets/img/livingarea6.jpg';
import livingarea7 from '../assets/img/livingarea7.jpeg';
import livingarea8 from '../assets/img/livingarea8.jpg';
import FooterComponent from './FooterComponent.vue';

export default {
  data() {
    const projects = [
      {
        id: 1,
        tag: "bedroom",
        img: bedroomProj1,
        header: "Minimal Bedroom",
        text: "Decor / Artchitecture"
      },
      {
        id: 2,
        tag: "bedroom",
        img: bedroomProj2,
        header: "Modern Bedroom",
        text: "Decor / Artchitecture"
      },
      {
        id: 3,
        tag: "bedroom",
        img: bedroomProj3,
        header: "System Table",
        text: "Decor / Artchitecture"
      },
      {
        id: 4,
        tag: "bedroom",
        img: bedroomProj4,
        header: "Modern Bedroom",
        text: "Decor / Artchitecture"
      },
      {
        id: 5,
        tag: "bedroom",
        img: bedroomProj5,
        header: "Modern Bedroom",
        text: "Decor / Artchitecture"
      },
      {
        id: 6,
        tag: "bedroom",
        img: bedroomProj6,
        header: "Modern Bedroom",
        text: "Decor / Artchitecture"
      },
      {
        id: 7,
        tag: "bedroom",
        img: bedroomProj7,
        header: "Modern Bedroom",
        text: "Decor / Artchitecture"
      },
      {
        id: 8,
        tag: "bedroom",
        img: bedroomProj8,
        header: "Modern Bedroom",
        text: "Decor / Artchitecture"
      },
      {
        id: 9,
        tag: "bathroom",
        img: bathroom1,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 10,
        tag: "bathroom",
        img: bathroom2,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 11,
        tag: "bathroom",
        img: bathroom3,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 12,
        tag: "bathroom",
        img: bathroom4,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 13,
        tag: "bathroom",
        img: bathroom5,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 14,
        tag: "bathroom",
        img: bathroom6,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 15,
        tag: "bathroom",
        img: bathroom7,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 16,
        tag: "bathroom",
        img: bathroom8,
        header: "Bathroom Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 17,
        tag: "kitchen",
        img: kitchan1,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 18,
        tag: "kitchen",
        img: kitchan2,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 19,
        tag: "kitchen",
        img: kitchan3,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 20,
        tag: "kitchen",
        img: kitchan4,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 21,
        tag: "kitchen",
        img: kitchan5,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 22,
        tag: "kitchen",
        img: kitchan6,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 23,
        tag: "kitchen",
        img: kitchan7,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 24,
        tag: "kitchen",
        img: kitchan8,
        header: "Kitchen Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 25,
        tag: "living",
        img: livingarea1,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 26,
        tag: "living",
        img: livingarea2,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 27,
        tag: "living",
        img: livingarea3,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 28,
        tag: "living",
        img: livingarea4,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 29,
        tag: "living",
        img: livingarea5,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 30,
        tag: "living",
        img: livingarea6,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 31,
        tag: "living",
        img: livingarea7,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
      {
        id: 32,
        tag: "living",
        img: livingarea8,
        header: "Living Area Design",
        text: "Decor / Artchitecture"
      },
    ];
    return {
      projects: projects,
      temp: [
        {
          id: 1,
          tag: "bedroom",
          img: bedroomProj1,
          header: "Minimal Bedroom",
          text: "Decor / Artchitecture"
        },
        {
          id: 2,
          tag: "bedroom",
          img: bedroomProj2,
          header: "Modern Bedroom",
          text: "Decor / Artchitecture"
        },
        {
          id: 3,
          tag: "bedroom",
          img: bedroomProj3,
          header: "System Table",
          text: "Decor / Artchitecture"
        },
        {
          id: 4,
          tag: "bedroom",
          img: bedroomProj4,
          header: "Modern Bedroom",
          text: "Decor / Artchitecture"
        },
        {
          id: 5,
          tag: "bedroom",
          img: bedroomProj5,
          header: "Modern Bedroom",
          text: "Decor / Artchitecture"
        },
        {
          id: 6,
          tag: "bedroom",
          img: bedroomProj6,
          header: "Modern Bedroom",
          text: "Decor / Artchitecture"
        },
        {
          id: 7,
          tag: "bedroom",
          img: bedroomProj7,
          header: "Modern Bedroom",
          text: "Decor / Artchitecture"
        },
        {
          id: 8,
          tag: "bedroom",
          img: bedroomProj8,
          header: "Modern Bedroom",
          text: "Decor / Artchitecture"
        },
      ],
    };
  },
  methods: {
    getProject(tag) {
      this.temp = this.projects.filter(item => item.tag === tag);
    },
    addFavourite(event) {
      const element = event.target;
      const parent = element.parentElement;
      const path = parent.getElementsByTagName('path');
      if (path[0].style.fill === "") {
        path[0].style.fill = "#FFA928";
      }
      else {
        path[0].style.fill = "";
      }
    }
  },
  components: { FooterComponent }
}
</script>

<style lang="scss" scoped>
.banner {
  background-image: url('../assets/img/bannerproject.png');
  background-repeat: no-repeat;
  height: 356px;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  margin-bottom: 200px;

  &-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #fff;
    padding: 41px 78px 41px 78px;
    border-top-left-radius: 40px;
    border-top-right-radius: 40px;

    &__title {
      color: #292F36;
      font-size: 50px;
      font-style: normal;
      font-weight: 400;
      line-height: 125%;
    }

    &__text {
      color: #4D5053;
      font-family: Jost;
      font-size: 22px;
      font-style: normal;
      font-weight: 400;
      line-height: 150%;
      letter-spacing: 0.22px;
    }
  }
}

.project {
  padding-left: calc(50% - 600px);
  padding-right: calc(50% - 600px);

  &-buttons {
    width: 880px;
    border: 1px solid #CDA274;
    border-radius: 18px;
    display: flex;
    flex-direction: row;
    align-content: center;
    justify-content: space-around;
    margin: 0 auto;
    margin-bottom: 61px;

    &__item {
      border: none;
      background-color: #fff;
      width: 219px;
      height: 75px;
      border-radius: 18px;
      font-family: "Jost";
      font-size: 18px;
      font-weight: 700;

    }

    &__item:hover {
      color: #fff;
      background-color: #CDA274;
      cursor: pointer;
    }
  }

  &-content {
    column-count: 2;
    column-gap: 0;

    &__item {
      break-inside: avoid;
      max-width: 563px;
      position: relative;
      margin-bottom: 36px;

      &-img {
        max-width: 100%;
        margin-bottom: 24px;
      }

      &-star {
        position: absolute;
        right: 5px;
        top: 5px;

        path {
          fill: rgb(199, 199, 199);
        }
      }

      &-textblock {
        display: flex;
        align-items: center;
        justify-content: space-between;

        &_item {
          &-title {
            font-family: 'DM Serif Display';
            font-size: 25px;
          }

          &-text {
            font-family: 'Jost';
            font-size: 22px;
          }
        }
      }
    }

    &__item:hover {
      cursor: pointer;
    }
  }
}

.pagination {
  padding-left: calc(50% - 600px);
  padding-right: calc(50% - 600px);
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 200px;
  margin-top: 61px;

  &-btn {
    width: 53px;
    height: 52px;
    flex-shrink: 0;
    border-radius: 50%;
    background-color: #fff;
    border: 1px solid #CDA274;
    color: #292F36;
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    text-transform: capitalize;
  }

  &-btn:hover {
    background-color: #F4F0EC;
    border: none;
    cursor: pointer;
  }

  &-img:hover {
    cursor: pointer;

    svg {
      circle {
        fill: #F4F0EC;
        stroke: none;
      }
    }
  }
}
</style>