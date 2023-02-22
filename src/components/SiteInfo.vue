<script>
import SiteInfoMobile from "./SiteInfoMobile.vue";

import SiteInfoTablet from "./SiteInfoTablet.vue";

import SiteInfoDesktop from "./SiteInfoDesktop.vue";

import Card from "./Card.vue";

export default {
  name: "SiteInfo",

  components: {
    SiteInfoMobile,

    SiteInfoTablet,

    SiteInfoDesktop,

    Card,
  },

  data() {
    return {
      list: [
        {
          title: "Background Information",

          content:
            "<div><h6>Predominant soil type: </h6> - </div><div><h6>Approximate date of site: </h6> - </div>",

          id: 2,

          idUp: "headingTwo",

          ariaExpanded: "false",

          dataTarget: "#collapseTwo",

          ariaControls: "collapseTwo",

          idDown: "collapseTwo",

          ariaLabelledby: "headingTwo",
        },

        {
          title: "Type of Project",

          content:
            "<div><h6>Evaluation </h6> </div><div><h6>Evaluation Site </h6></div>",

          ariaExpanded: "false",

          id: 3,

          idUp: "headingThree",

          dataTarget: "#collapseThree",

          ariaControls: "collapseThree",

          idDown: "collapseThree",

          ariaLabelledby: "headingThree",
        },
        {
          title: "Manage number ranges",
          content: "<p>-</p>",
          id: 4,
          idUp: "headingFour",
          ariaExpanded: "false",
          dataTarget: "#collapseFour",
          ariaControls: "collapseFour",
          idDown: "collapseFour",
          ariaLabelledby: "headingFour",
        },
      ],
    };
  },
};
</script>

<template>
  <div>
    <!-- <div id="content" v-html="content"></div> -->

    <div>Script Info here</div>

    <SiteInfoMobile :list="list" class="mobile" />

    <SiteInfoTablet :list="list" class="tablet" />

    <SiteInfoDesktop :list="list" class="desktop" />
  </div>
</template>

<style>
h6 {
  display: inline-block;
}

.class-button.styled-button {
  border: 4px solid #5d3f6a;

  border-radius: 10px;

  background-color: rebeccapurple;

  margin-left: -10px;
}

/* button{

background-color: #fff;

border: 3px solid #5d3f6a;

border-radius: 10px;

margin-right: 10px;

} */

body {
  background-color: #f7f7f7 !important;
}

@media screen and (min-width: 280px) {
  .desktop {
    display: none;
  }

  .tablet {
    display: none;
  }
}

@media screen and (min-width: 700px) {
  .mobile {
    display: none;
  }

  .desktop {
    display: none;
  }

  .tablet {
    display: block;

    height: 650px;

    border: 2px solid red;

    align-content: center;
  }
}

@media screen and (min-width: 1200px) {
  .mobile {
    display: none;
  }

  .tablet {
    display: none;
  }

  .desktop {
    display: block;

    height: 500px;

    border: 2px solid red;

    align-content: center;

    width: 1500px;

    position: absolute;

    top: 200px;

    left: 200px;
  }
}
</style>
