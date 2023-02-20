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
      List: [
        {
          Title: "Project Details",
          Content:
            '<div><h6>Project Name:</h6><span> Land West of North Ockendon </span><br><h6>Invoice Codes:</h6> LTC40NEV <br><h6>Cost Center:</h6> OXF<br><h6> Project Manager:</6> Steve Lawrence</h6><br><h6>Address:</h6> Lower Thames Crossing land west of North Ockendon<br> <h6>Project Webmap:</h6>  <a href="https://webmap.oxfordarchaeology.com/LTC71R20" target="_blank"><button>Click to see the map </button>',
          id: 1,
          idUp: "headingOne",
          ariaExpended: "true",
          dataTarget: "#collapseOne",
          ariaControls: "collapseOne",
          idDown: "collapseOne",
          ariaLabelledby: "headingOne"
        },
        {
          Title: "Background Information",
          Content:
            '<div><h6>Predominant soil type: </h6> - </div><div><h6>Approximate date of site: </h6> - </div>',
          id: 2,
          idUp: "headingTwo",
          ariaExpended: "false",
          dataTarget: "#collapseTwo",
          ariaControls: "collapseTwo",
          idDown: "collapseTwo",
          ariaLabelledby: "headingTwo"
        },
        {
          Title: "Type of Project",
          Content: '<div><h6>Evaluation </h6> </div><div><h6>Evaluation Site </h6></div>',
          ariaExpended: "false",
          id: 3,
          idUp: "headingThree",
          dataTarget: "#collapseThree",
          ariaControls: "collapseThree",
          idDown: "collapseThree",
          ariaLabelledby: "headingThree"
        },
        {
          Title: "Trenches",
          Content:
           '<div class="class-button"><button class="styled-button"> View Report</button> <button class="styled-button"> Thrences Register</button><Br> <h6> Number of thrences:</h6> 144 <br><button class="styled-button"> Context Numbers</button><br> <button class="styled-button">Export Contexts to Excel </button><br> <button class="styled-button">Export Thrench Tables to Excel </button> <br><button class="styled-button">Export Trench Register to Excel </button></div>',
          id: 4,
          idUp: "headingFour",
          ariaExpended: "false",
          dataTarget: "#collapseFour",
          ariaControls: "collapseFour",
          idDown: "collapseFour",
          ariaLabelledby: "headingFour"
        },

        {
          Title: 'Manage number ranges',
          Content: "<p>-</p>",
          id: 5,
          idUp: "headingFive",
          ariaExpended: "false",
          dataTarget: "#collapseFive",
          ariaControls: "collapseFive",
          idDown: "collapseFive",
          ariaLabelledby: "headingFive"
        },
        {
          Title: "Environmental Samples",
          Content:
            '<p>  <strong>Range: </strong>starts from <strong>1</strong> and ends at <strong>30</strong>.</p> <button> Sample Numbers </button> <button>Export Samples to Excel</button>',
          id: 6,
          idUp: "headingSix",
          ariaExpended: "false",
          dataTarget: "#collapseSix",
          ariaControls: "collapseSix",
          idDown: "collapseSix",
          ariaLabelledby: "headingSix"
        },
        {
          Title: 'Stratigraphic relationships',
          Content:
            '<button>View All</button> <button> Export Stratigraphic Relationships to Excel </button>',
          id: 7,
          idUp: "headingSeven",
          ariaExpended: "false",
          dataTarget: "#collapseSeven",
          ariaControls: "collapseSeven",
          idDown: "collapseSeven",
          ariaLabelledby: "headingSeven"
        },
        {
          Title: "Export Data",
          Content:
            '<button>Export Spot Dates to Excel</button><br><button>Export Photogrammetry to Excel</button><br><button>Export for Deposition</button>',
          id: 8,
          idUp: "headingEight",
          ariaExpended: "false",
          dataTarget: "#collapseEight",
          ariaControls: "collapsEighte",
          idDown: "collapseEight",
          ariaLabelledby: "headingEight"
        },
      ],
    };
  },
};
</script>
<template>
  <div>
    <!-- <div id="content" v-html="Content"></div> -->

    <div>Script Info here</div>
    <SiteInfoMobile 
    v-bind:List="List" class="mobile">MOBILE 
    </SiteInfoMobile>
    <SiteInfoTablet
      v-bind:List="List"
      class="tablet">
      TABLET
      </SiteInfoTablet
    >
    <SiteInfoDesktop 
    v-bind:List="List" class="desktop">
    DESKTOP
      </SiteInfoDesktop
    >
  </div>
</template>
<style>

 h6 {
    display: inline-block;
}
.class-button.styled-button{
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
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(50%, 1fr));
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
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(33%, 1fr));
    height: 500px;
    border: 2px solid red;
    align-content: center;
    width: 1500px;
    position: absolute;
    top: 200px;
    left: 200px
  }
 
}
</style>
