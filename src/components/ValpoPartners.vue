<template>
  <section id="partners" class="partners content flex-around">
    <valpo-list class="icons flex-center">
      <valpo-list-item v-for="(item) in ourPartners" :key="item.icon">
        <figure>
          <img v-lazy="item.icon" :alt="item.alt">
        </figure>
      </valpo-list-item>
    </valpo-list>
  </section>
</template>

<script>
import north53 from "../assets/images/partners/53gradennoord.jpg";
import azart from "../assets/images/partners/Azart_partners.png";
import elektro from "../assets/images/partners/elektro_producten_partners.png";
import glas from "../assets/images/partners/glas_in_lood_boot_partners.png";
import horeca from "../assets/images/partners/horeca_partners.png";
import leds4life from "../assets/images/partners/leds4life_partners.png";
import zeeds from "../assets/images/partners/zeeds_partners.png";
import erasmusplus from "../assets/images/partners/erasmusplus.png";
import eurocommission from "../assets/images/partners/european_commission.png";
import tastebefore from "../assets/images/partners/tastebefore.jpg";


import ValpoList from "@/components/ValpoList";
import ValpoListItem from "@/components/ValpoListItem";

export default {
  name: "Partners",
  components:{ ValpoList, ValpoListItem },
  data: () => ({
    images: {
        north53,
        azart,
        elektro,
        glas,
        horeca,
        leds4life,
        zeeds,
        erasmusplus,
        eurocommission,
        tastebefore
    },
    ourPartners: [
      {
        icon: north53,
        alt: "53 Nord"
      },
      {
        icon: azart,
        alt: "Azart"
      },
      {
        icon: elektro,
        alt: "Elektro Producten"
      },
      {
        icon: glas,
        alt: "Glas in Loot Boot"
      },
      {
        icon: tastebefore,
        alt: "Taste Before You Waste"
      },
      {
        icon: leds4life,
        alt: "Leds 4 Life"
      },
      {
        icon: zeeds,
        alt: "Zeedruk"
      },
      {
        icon: erasmusplus,
        alt: "Erasmus+"
      },
      {
        icon: eurocommission,
        alt: "European Commission"
      },
      {
        icon: horeca,
        alt: "Horeka"
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
.partners {
  background: var(--color-cerulean);
  font-size: 0.9em;
  margin: 0 auto;
  max-width: var(--wrapper-width);
  min-height: 10vh;
  padding-top: calc(var(--tracking-large) * 5);
  padding: 1em;
  position: relative;
  width: 100%;
  @media (max-width: 680px) {
    flex-direction: column-reverse;
  }
  p {
    width: 33%;
    @media (max-width: 680px) {
      text-align: center;
      width: 100%;
    }
  }
  img {
    margin-top: calc(var(--tracking-large) * 1);
    max-width: 80px;
  }
  img[alt="53 Nord"] {
    border-radius: 10px;
  }
  img[alt="Aweken & More"] {
    max-width: 110px
  }
  .valpo-list {
    margin: 1em 0;
  }
  .valpo-list-item {
    margin: 0 1vw;
    vertical-align: middle;
    @media (max-width: 550px) {
      max-width: 40%;
    }
    figure {
      @media (max-width: 550px) {
        margin: .5em auto;
      }
    }
  }
}
</style>
