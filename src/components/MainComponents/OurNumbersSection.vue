<template>
  <section id="results-section">
    <div class="container flex-center">
      <div class="row col-10 text-center justify-content-center">

        <SectionsHeadings :info="titleInfo" />

        <div class="result col-2 mx-4 mt-5"
          v-for="(result, index) in companyResults"
          :key="index">
          <h2>{{ result.number }}</h2>
          <p>{{ result.area }}</p>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
import SectionsHeadings from "./SectionsHeadings.vue";

export default {
  name: "OurNumbersSection",
  components: {
    SectionsHeadings,
  },
  data: function () {
    return {
      titleInfo: {
        topSubtitle: "what are we doing",
        title: "results in numbers",
        description: false,
        typeOne: false,
        typeTwo: true,
      },
      companyResults: [
        {
          number: "128",
          area: "certifications",
        },
        {
          number: "230",
          area: "employees",
        },
        {
          number: "517",
          area: "customers",
        },
        {
          number: "94",
          area: "countries served",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
    @import "../../scss/style.scss";

    #results-section {
    background-image: url("../../assets/backgrounds/bg-7.jpg");
    padding: 6rem 0;
        .result {
            h2 {
            color: $brandTextColorLight;
            font-weight: bolder;
            }
            p {
            text-transform: capitalize;
            font-weight: bold;
            color: $lightTextColor;
            }
        }
    }
</style>