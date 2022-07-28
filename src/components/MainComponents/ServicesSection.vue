<template>
  <section id="services" class="container-fluid">
    <div class="container">
      <div class="row col-10 offset-1">

        <div class="col-8 m-auto">
          <SectionsHeadings :info="titleInfo" />
        </div>
        
        <div class="col-3 d-flex align-items-end justify-content-end">
          <a
            class="text-uppercase btn activeGreenLink px-4 mb-4 me-4"
            @click.prevent
            href="#"
            >see all</a
          >
        </div>
      </div>
      <div class="row gap-3 justify-content-center mt-3">
        <div
          v-for="(card, index) in servicesInfos"
          :key="index"
          class="col-3 services-card rounded">
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
    </div>
  </section>
</template>

<script>
import SectionsHeadings from "./SectionsHeadings.vue";

export default {
  name: "ServicesSection",
  components: {
    SectionsHeadings,
  },
  methods: {
    iconPath: function (object) {
      return "bi bi-" + object.icon;
    },
  },
  data: function () {
    return {
      titleInfo: {
            topSubtitle: "our business area",
            title: "exellence in",
            brandTitle: "services",
            description: 'We are leaders in providing consultancy services with a set of cutting-edge technologies ans a team of experienced and renowned professionals. These are some options that you can hire',
            typeOne: true,
            typeTwo: false,
      },
      servicesInfos: [
        {
          icon: "hdd-network",
          title: "audit & assurance",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
          url: "#",
        },
        {
          icon: "briefcase",
          title: "financial advisory",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
          url: "#",
        },
        {
          icon: "bar-chart",
          title: "analitics and m&a",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
          url: "#",
        },
        {
          icon: "airplane",
          title: "middle marketing",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
          url: "#",
        },
        {
          icon: "globe",
          title: "legal consulting",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
          url: "#",
        },
        {
          icon: "inbox",
          title: "regulatory risk",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../../scss/style.scss";
#services {
  background-color: $ServicesBg;
  padding: 8rem 0;

  .services-card {
    padding: 1.8rem;
    background-color: $CcWhite;

    i {
      font-size: 2rem;
      color: $CcBluelagoon;
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
}
</style>