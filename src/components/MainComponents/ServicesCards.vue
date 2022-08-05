<template>
  <div class="col-4 p-3">
    <div class="services-card rounded p-4">
      <div class="d-flex justify-content-between">
        <i :class="iconPath(cardInfos)"></i>
        <a :href="cardInfos.url" @click.prevent>
          <i class="bi bi-arrow-right-short"></i>
        </a>
      </div>
      <h5>{{ cardInfos.title }}</h5>
      <p class="card-text">{{ cardInfos.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServicesCard",
  props: {
    cardInfos: Object,
  },
  methods: {
    iconPath: function (object) {
      return "bi bi-" + object.icon;
    },
  },
};
</script>

<style lang="scss">
  @import "../../scss/style.scss";

  .services-card {
    background-color: $lightTextColor;
    transition: transform 200ms linear;

    i {
      font-size: 2rem;
      color: $brandTextColor;
    }

    h5 {
      text-transform: capitalize;
      padding: 1.2rem 0;
    }

    a {
      display: none;
      opacity: 0.6;
    }

    &:hover a {
      display: inline-block;
    }
    &:hover {
      transform: translate(0, -10%);
    }
  }
</style>