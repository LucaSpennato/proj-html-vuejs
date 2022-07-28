<template>
  <section id="about-company">
    <div class="container row m-auto">
      <div class="left-col col-4 offset-2">
            <div class="infos">
              <h6 class="text-uppercase">about the network</h6>
              <h1 class="fw-bold py-4">
                <span>The</span>
                Company
              </h1>
              <p>
                For 12 years we have been rpviding audit and warranty, financial
                advice, risk advice, taxes and related services to select
                clients.
              </p>
            </div>
            <div class="cards">
              <div
                class="about-card"
                v-for="(card, index) in aboutTheCompanyInfos"
                :key="index">
                <i :class="iconPath(card)"></i>
                <h5>
                  {{ card.title }}
                </h5>
                <p>
                  {{ card.text }}
                </p>
              </div>
            </div>
            <div>
              <a class="btn" href="#">get in touch</a>
              <a class="btn" href="#">read more</a>
            </div>
      </div>
      <div class="side-imgs col-6 p-0">
        <img
          
          :src="require('../../assets/backgrounds/about-4.jpg')"
          alt="about-image"
        />
        <div class="right-column">
          <img
            :src="require('../../assets/general/bullets.png')"
            alt="style-dots"
          />
          <img
            :src="require('../../assets/general/bullets.png')"
            alt="style-dots"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutTheCompany",
  methods: {
    iconPath: function (object) {
      return "bi bi-" + object.icon;
    },
  },
  data: function () {
    return {
      aboutTheCompanyInfos: [
        {
          icon: "award",
          title: "tradition",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "lock",
          title: "security",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "pencil-square",
          title: "certificate",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "mortarboard",
          title: "expertise",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
    @import "../../scss/style.scss";
    #about-company {
    background-color: $CcWoodsmoke;
    position: relative;
    
    .infos {
        h1 {
        color: white;
        }
        span {
        @include companyStyledWordBg;
        }
        h6 {
        color: $CcBluelagoon;
        font-size: 0.8rem;
        }
        p {
        color: $CcPumice;
        }
    }
    .left-col{
        margin-top: 4rem;
    }
    .about-card {
        display: inline-block;
        width: calc((100% / 2) - 0.6rem);
        margin-left: 0.3rem;
        margin-top: 1.7rem;
        i {
        color: $CcBluelagoon;
        font-size: 1.3rem;
        }
        h5 {
        display: inline;
        color: $CcWhite;
        text-transform: capitalize;
        margin-left: 0.3rem;
        }
        p {
        margin-top: 1rem;
        color: $CcPumice;
        }
    }
    a {
        @include inactiveElementGreen;

        &:hover {
        @include activeElementGreen;
        }
    }
    .side-imgs{
        img{
            width: 47.5rem;
            height: 43rem;
            object-fit: cover;
        }
    }
    .right-column {
        img {
        position: absolute;
        width: 7rem;
        height: 3rem;
        object-fit: cover;
        transform: translate(-50%, -50%);
        left: 50%;
        opacity: 0.3;
        }
        img:nth-child(1) {
        top: -3px;
        }
        img:nth-child(2) {
        bottom: -2.8rem;
        }
    }
    }
</style>