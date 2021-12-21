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
          <div class="imgs__mainWrapper col-sm-9 mx-auto">
            <figure class="img__mainGif w-100">
              <img class="w-100" src="../assets/header/main-gif.gif" alt="" />
            </figure>
            <figure class="img__dots">
              <img src="../assets/header/Dots.png" alt="" />
            </figure>
            <figure class="img__ellipse">
              <img src="../assets/header/Ellipse.png" alt="" />
            </figure>
          </div>
        </div>
      </div>
    </header>
    <section class="what__youNeed">
      <div class="container-fluid">
        <div class="row">
          <div class="need__list col-sm-5">
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
          <div class="imgs__SubWrapper col-sm-7 mx-auto">
            <figure class="img__subGif">
              <img class="w-100" src="../assets/body/sub-gif.gif" alt="" />
            </figure>
            <figure class="img__dots">
              <img src="../assets/header/Dots.png" alt="" />
            </figure>
            <figure class="img__ellipse">
              <img src="../assets/header/Ellipse.png" alt="" />
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
/* // @include responsiveScreen($smallScreen) {
// } */
.page__header {
  padding-top: 30px;
  padding-bottom: 110px;
  h1 {
    font-size: 36px;
    font-weight: 700;
    color: #8d5da7;
    margin-bottom: 20px;
  }
  p {
    font-size: 18px;
    line-height: 34px;
    margin-bottom: 40px;
  }
  .page__appLinkWrapper {
    margin-bottom: 85px;
  }
  .imgs__mainWrapper {
    position: relative;
    .img__mainGif {
      height: 550px;
      z-index: 2;
      img {
        border-radius: 40px;
        height: 100%;
        object-fit: cover;
      }
    }
    .img__dots {
      position: absolute;
      top: -40px;
      left: -70px;
      z-index: -1;
    }
    .img__ellipse {
      position: absolute;
      bottom: -93px;
      right: -81px;
      z-index: -1;
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
      color: #8d5da7;
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
  }
  .imgs__SubWrapper {
    position: relative;
    z-index: 10;
    .img__subGif {
      z-index: 2;
      height: 440px;
      width: 96%;
      img {
        border-radius: 40px;
        height: 100%;
      }
    }
    .img__dots {
      position: absolute;
      top: -40px;
      left: 0px;
      z-index: -1;
    }
    .img__ellipse {
      position: absolute;
      bottom: -84px;
      right: -45px;
      z-index: -1;
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
}
</style>
