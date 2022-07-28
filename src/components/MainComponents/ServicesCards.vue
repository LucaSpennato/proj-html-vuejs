<template>
  <div class="row gap-3 justify-content-center mt-3">
        <div
          v-for="(card, index) in cardsInfo"
          :key="index"
          class="col-3 p-4 services-card rounded">
          <div>
            <div class="d-flex justify-content-between">
              <i :class="iconPath(card)"></i>
              <a :href="card.url" @click.prevent>
                <i class="bi bi-arrow-right-short"></i>
              </a>
            </div>
            <h5>{{ card.title }}</h5>
            <p class="card-text">{{ card.text }}</p>
          </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'ServicesCard',
    props:{
        cardsInfo: Array,
    },
      methods: {
        iconPath: function (object) {
            return "bi bi-" + object.icon;
        },
    },
}
</script>

<style lang="scss">
    @import "../../scss/style.scss";

    .services-card {
        background-color: $lightTextColor;

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
  }
</style>