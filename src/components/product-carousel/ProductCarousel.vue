<template>
  <div class="container mt-5">
    <div class="owl-carousel owl-product-carousel owl-theme" v-if="cardMockups">
      <Card
        class="item"
        style="width: 21rem;"
        v-for="cardMockup in cardMockups"
        :key="cardMockup.id"
        :cardMockup="cardMockup"
      />
    </div>
  </div>
</template>

<script>
import owlCarousel from "@/assets/js/owlCarousel.js";
import Card from "../card/Card";
export default {
  components: {
    Card,
  },
  data() {
    return {
      cardMockups: [
        {
          id: 1,
          title: "Blue silk flare sleeved top",
          image: "sleeved-top.svg",
          badge: "New",
          badge2: "",
          productInfo: "New look men´s coat",
          category: "Fashion",
          oldPrice: "$220.00",
          newPrice: "$190.00",
        },
        {
          id: 2,
          title: "Another great product",
          image: "sleeved-top.svg",
          badge: "-25%",
          badge2: "",
          productInfo: "New fresh look",
          category: "Fresh",
          oldPrice: "$500.00",
          newPrice: "$390.00",
        },
        {
          id: 3,
          title: "Wow!",
          image: "pattern-shirt.svg",
          badge: "Hot",
          badge2: "",
          productInfo: "New look men´s coat",
          category: "Fashion",
          oldPrice: "$220.00",
          newPrice: "$190.00",
        },
        {
          id: 4,
          title: "Another great product",
          image: "sleeved-top.svg",
          badge: "New",
          badge2: "-25%",
          productInfo: "New fresh look",
          category: "Fresh",
          oldPrice: "$500.00",
          newPrice: "$390.00",
        },
        {
          id: 5,
          title: "Blue silk flare sleeved top",
          image: "sleeved-top.svg",
          badge: "",
          badge2: "",
          productInfo: "New look men´s coat",
          category: "Fashion",
          oldPrice: "$220.00",
          newPrice: "$190.00",
        },
        {
          id: 6,
          title: "Another great product",
          image: "sleeved-top.svg",
          badge: "Hot",
          badge2: "",
          productInfo: "New fresh look",
          category: "Fresh",
          oldPrice: "$500.00",
          newPrice: "$390.00",
        },
      ],
    };
  },
};
</script>

<style>
.owl-prev,
.owl-next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  display: block !important;
  color: #e3e3e3 !important;
}

.owl-prev {
  left: -8%;
}

.owl-next {
  right: -6%;
}

.owl-prev i,
.owl-next i {
  font-size: 2.2rem;
  padding: 1rem 1.4rem;
  border: 2px solid #e3e3e3;
  border-radius: 50% !important;
}

.owl-prev i:hover,
.owl-next i:hover {
  background: var(--theme-color) !important;
  border: transparent !important;
}

.owl-nav button.owl-prev:hover,
.owl-nav button.owl-next:hover {
  background: none !important;
}

.owl-theme .owl-dots .owl-dot.active span {
  background: var(--theme-color);
}
</style>