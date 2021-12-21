<template>
  <div class="landing__page">
    <header class="page__header text-center">
      <div class="container">
        <h1 class="">طور متجرك ووسع افاق تجارتك مع سوق تطبيقات زد</h1>
        <p class="w-50 mx-auto">
          طور تجارتك من خلال تطبيقات وحلول سوق تطبيقات زد التي تساعك في نمو
          أرباحك عبر إدارة عمليات متجرك بشكل فعال واحترافي
        </p>
        <AllAppsLink />
        <div class="row">
          <div class="imgs__mainWrapper col-sm-12 col-md-10 col-lg-8 mx-auto">
            <figure class="img__mainGif mb-0">
              <img
                class="img__gif w-100"
                src="../assets/header/main-gif.gif"
                alt=""
              />
              <img class="img__dots" src="../assets/header/Dots.png" alt="" />
              <img
                class="img__ellipse"
                src="../assets/header/Ellipse.png"
                alt=""
              />
            </figure>
          </div>
        </div>
      </div>
    </header>
    <section class="what__youNeed">
      <div class="container-fluid">
        <div class="row">
          <div
            class="need__list col-sm-12 col-md-10 col-lg-5 order-sm-2 order-lg-1 mx-auto"
          >
            <h2>كل ما تحتاجة لنمو متجرك في مكان واحد</h2>
            <p>
              مميزات سوق تطبيقات زد تساعدك في سهولة وسرعة الاستفادة من خدمات
              وحلول سوق التطبيقات لنمو متجرك ومضاعفة أرباحك
            </p>
            <ul class="list__features list-unstyled pe-0">
              <li class="d-flex align-items-center">
                <figure
                  class="ps-1 d-flex justify-content-center align-items-center"
                >
                  <img src="../assets/icon/vector-1.png" alt="" />
                </figure>
                <p class="pe-3">
                  سهولة ادارة وتفعيل تطبيقاتك من نفس لوحة تحكم متجرك
                </p>
              </li>
              <li class="d-flex align-items-center">
                <figure
                  class="ps-1 d-flex justify-content-center align-items-center"
                >
                  <img src="../assets/icon/vector-2.png" alt="" />
                </figure>
                <p class="pe-3">دعم فني وتقني متكامل متوفر علي مدار الساعة</p>
              </li>
              <li class="d-flex align-items-center">
                <figure
                  class="ps-1 d-flex justify-content-center align-items-center"
                >
                  <fa :icon="['fas', 'hand-holding-usd']" />
                </figure>
                <p class="pe-3">
                  أسعار تنافسية مع تجربة مجانية وباقات اشتراك متنوعة
                </p>
              </li>
            </ul>
            <AllAppsLink />
          </div>
          <div
            class="imgs__SubWrapper col-sm-11 col-md-10 col-lg-7 mx-auto order-sm-1 order-lg-2 mx-auto"
          >
            <figure class="img__subGif">
              <img
                class="img__gif w-100"
                src="../assets/body/sub-gif.gif"
                alt=""
              />
              <img class="img__dots" src="../assets/header/Dots.png" alt="" />
              <img
                class="img__ellipse"
                src="../assets/header/Ellipse.png"
                alt=""
              />
            </figure>
          </div>
        </div>
      </div>
    </section>
    <section class="special__apps text-center">
      <div class="container">
        <h2>التطبيقات المتميزة</h2>
        <p>تطبيقات تقدم حلول وخدمات مميزة نوصي بتجربتها</p>
        <div class="row">
          <SpecialApps
            v-for="app in specialApps"
            :key="app.id"
            :name="app.name"
            :rate="app.rate"
            :devBy="app.devBy"
            :description="app.description"
          />
        </div>
      </div>
      <AllAppsLink />
    </section>
  </div>
</template>

<script>
const specialApps = [
  {
    id: 1,
    name: "قمرة",
    rate: "5",
    devBy: "عمر برهوم",
    description: "نظام الولاء الأمثل الذي يمكنك من رفع مبيعاتك.",
  },
  {
    id: 2,
    name: "قمرة",
    rate: "5",
    devBy: "عمر برهوم",
    description: "نظام الولاء الأمثل الذي يمكنك من رفع مبيعاتك.",
  },
  {
    id: 3,
    name: "قمرة",
    rate: "5",
    devBy: "عمر برهوم",
    description: "نظام الولاء الأمثل الذي يمكنك من رفع مبيعاتك.",
  },
  {
    id: 4,
    name: "قمرة",
    rate: "5",
    devBy: "عمر برهوم",
    description: "نظام الولاء الأمثل الذي يمكنك من رفع مبيعاتك.",
  },
];
import SpecialApps from "../components/SpecialApps.vue";
import AllAppsLink from "../components/AllAppsLink.vue";
export default {
  data() {
    return {
      specialApps,
    };
  },
  name: "LandingPage",
  components: {
    SpecialApps,
    AllAppsLink,
  },
};
</script>

<style lang="scss">
.page__header {
  padding-top: 30px;
  padding-bottom: 203px;
  h1 {
    font-size: 36px;
    font-weight: 700;
    color: #8d5da7;
    margin-bottom: 20px;
  }
  p {
    font-size: 18px;
    line-height: 34px;
    margin-bottom: 45px;
    @include responsiveScreen($smallScreen) {
      width: 90% !important;
    }
    @include responsiveScreen($mediumScreen) {
      width: 95% !important;
    }
    @include responsiveScreen($largeScreen) {
      width: 95% !important;
    }
    @include responsiveScreen($extraLargeScreen) {
      width: 65% !important;
    }
  }
  .page__appLinkWrapper {
    margin-bottom: 100px;
  }
  .imgs__mainWrapper {
    .img__mainGif {
      height: 550px;
      position: relative;
      z-index: 2;
      .img__gif {
        border-radius: 40px;
        height: 100%;
        object-fit: cover;
      }
      .img__dots {
        width: 164px;
        height: 179px;
        position: absolute;
        top: -35px;
        left: -65px;
        z-index: -1;
      }
      .img__ellipse {
        width: 367px;
        height: 367px;
        position: absolute;
        bottom: -93px;
        right: -81px;
        z-index: -1;
      }
      @include responsiveScreen($mediumScreen) {
        .img__dots {
          left: -25px;
        }
        .img__ellipse {
          bottom: -80px;
          right: -25px;
        }
      }
    }
    @include responsiveScreen($smallScreen) {
      width: 90%;
      .img__mainGif {
        .img__dots {
          left: -37px;
        }
        .img__ellipse {
          bottom: -65px;
          right: -35px;
        }
      }
    }
  }
}

.what__youNeed {
  padding-top: 58px;
  padding-bottom: 58px;
  background-color: #fafafc;
  .need__list {
    padding-right: 25px;
    h2 {
      font-size: 24px;
      font-weight: 700;
      color: $mainColor;
      margin-bottom: 20px;
      + p {
        font-size: 16px;
        font-weight: 400;
        line-height: 30px;
        margin-bottom: 20px;
      }
    }
    .list__features {
      margin-bottom: 40px;
      figure {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background-color: white;
        svg {
          color: $mainColor;
        }
      }
      p {
        font-size: 15px;
        font-weight: 600;
      }
      li:last-child {
        p {
          font-size: 12px;
        }
      }
    }
    .page__appLinkWrapper {
      margin-bottom: 0;
    }
    @include responsiveScreen($smallScreen) {
      order: 2;
      text-align: center;
    }
    @include responsiveScreen($mediumScreen) {
      text-align: center;
    }
    @include responsiveScreen($largeScreen) {
      text-align: center;
    }
  }
  .imgs__SubWrapper {
    z-index: 10;
    .img__subGif {
      z-index: 2;
      height: 440px;
      width: 96%;
      position: relative;
      .img__gif {
        border-radius: 40px;
        height: 100%;
      }
      .img__dots {
        position: absolute;
        top: -42px;
        left: -39px;
        z-index: -1;
      }
      .img__ellipse {
        position: absolute;
        bottom: -84px;
        right: -55px;
        z-index: -1;
      }
      @include responsiveScreen($mediumScreen) {
        width: 100%;
        margin-bottom: 100px;
        .img__dots {
          left: -25px;
        }
        .img__ellipse {
          bottom: -80px;
          right: -25px;
        }
      }
      @include responsiveScreen($largeScreen) {
        margin-bottom: 100px;
      }
    }
    @include responsiveScreen($smallScreen) {
      order: 1;
      width: 90%;
      margin-bottom: 100px;
      .img__subGif {
        width: 100%;
        .img__dots {
          left: -37px;
        }
        .img__ellipse {
          bottom: -65px;
          right: -35px;
        }
      }
    }
  }
}

.special__apps {
  padding-top: 190px;
  padding-bottom: 120px;
  h2 {
    font-size: 24px;
    font-weight: 600;
    margin-bottom: 10px;
    + p {
      font-size: 14px;
      margin-bottom: 40px;
    }
  }
  .page__appLinkWrapper {
    margin-top: 40px;
    .page__appLink {
      background-color: white;
      span {
        font-size: 16px;
        font-weight: 400;
        &:last-child {
          font-size: 14px;
          padding-right: 10px;
        }
      }
    }
  }
  @include responsiveScreen($smallScreen) {
    padding-top: 50px;
  }
  @include responsiveScreen($mediumScreen) {
    padding-top: 50px;
  }
  @include responsiveScreen($largeScreen) {
    padding-top: 50px;
  }
}
</style>
