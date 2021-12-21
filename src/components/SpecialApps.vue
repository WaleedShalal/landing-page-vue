<template>
  <div class="app__infoWrapper col-sm-12 col-md-6 col-xl-3 py-1">
    <div class="app__info d-flex">
      <figure class="flex-shrink-0">
        <img src="../assets/body/special-app.png" alt="..." />
      </figure>
      <div class="flex-grow-1 me-3">
        <div class="app__infoName d-flex flex-column">
          <div class="d-flex align-items-baseline">
            <h5>{{ name }}</h5>
            <div class="app__infoRate">
              <span>
                <fa :icon="['fas', 'star']" />
              </span>
              <span>{{ rate }}</span>
            </div>
          </div>
          <div class="app__infoDevBy d-flex">
            <h6>
              <span>تطوير : </span> <span> {{ devBy }} </span>
            </h6>
          </div>
        </div>
        <div class="app__infoDescription d-flex flex-column text-end">
          <p class="mb-2">{{ description }}</p>
          <p class="mb-0">{{ description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["name", "rate", "devBy", "description"],
  name: "SpecialApps",
};
</script>

<style lang="scss" scoped>
.app__info {
  background-color: #f7f7f7;
  border-radius: 10px;
  padding: 30px 23px;
  .app__infoName {
    margin-bottom: 16px;
    h5 {
      font-size: 16px;
      font-weight: 600;
      color: $mainColor;
      margin-bottom: 11px;
    }
    .app__infoRate {
      padding-right: 22px;
      span:first-child {
        color: #ffd12f;
        font-size: 13px;
      }
      span:last-child {
        color: #45a787;
        font-size: 14px;
        padding-right: 5px;
      }
    }
    .app__infoDevBy {
      h6 {
        font-size: 14px;
        span:first-child {
          font-weight: 600;
        }
        span:last-child {
          color: #6d6d6d;
        }
      }
    }
  }
  .app__infoDescription {
    p {
      font-size: 12px;
    }
  }
}
</style>
