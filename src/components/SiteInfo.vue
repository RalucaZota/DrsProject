<script>
import SiteInfoMobile from "./SiteInfoMobile.vue";
import SiteInfoTablet from "./SiteInfoTablet.vue";
import SiteInfoDesktop from "./SiteInfoDesktop.vue";


export default {
  name: "SiteInfo",
  components: { SiteInfoMobile, SiteInfoTablet, SiteInfoDesktop},

  data() {
    return {
      list: [
        // {
        //   title: "Project Details",
        //   content:
        //     '<div><h6>Project Name:</h6><span> Land West of North Ockendon </span><br><h6>Invoice Codes:</h6> LTC40NEV <br><h6>Cost Center:</h6> OXF<br><h6> Project Manager:</6> Steve Lawrence</h6><br><h6>Address:</h6> Lower Thames Crossing land west of North Ockendon<br> <h6>Project Webmap:</h6> <a href="https://webmap.oxfordarchaeology.com/LTC71R20" target="_blank"><button>Click to see the map </button>',
        //   id: 1,
        //   idUp: "headingOne",
        //   ariaExpended: "true",
        //   dataTarget: "#collapseOne",
        //   ariaControls: "collapseOne",
        //   idDown: "collapseOne",
        //   ariaLabelledby: "headingOne",
        // },
        {
          title: "Background Information",
          content:
            '<div><div><h6>Predominant soil type: </h6> - </div><div><h6>Approximate date of site: </h6> - </div></div>',
          id: 2,
          idUp: "headingTwo",
          ariaExpended: "false",
          dataTarget: "#collapseTwo",
          ariaControls: "collapseTwo",
          idDown: "collapseTwo",
          ariaLabelledby: "headingTwo",
        },
        {
          title: "Type of Project",
          content:
            "<div><h6>Evaluation </h6> </div><div><h6>Evaluation Site </h6></div>",
          ariaExpended: "false",
          id: 3,
          idUp: "headingThree",
          dataTarget: "#collapseThree",
          ariaControls: "collapseThree",
          idDown: "collapseThree",
          ariaLabelledby: "headingThree",
        },
        // {
        //   title: "Trenches",
        //   content:
        //     '<div class="class-button"><button class="styled-button"> View Report</button> <button class="styled-button"> Trenches Register</button><Br> <h6> Number of trenches:</h6> 144 <br><button class="styled-button"> Context Numbers</button><br> <button class="styled-button">Export Contexts to Excel </button><br> <button class="styled-button">Export Trench Tables to Excel </button> <br><button class="styled-button">Export Trench Register to Excel </button></div>',
        //   id: 4,
        //   idUp: "headingFour",
        //   ariaExpended: "false",
        //   dataTarget: "#collapseFour",
        //   ariaControls: "collapseFour",
        //   idDown: "collapseFour",
        //   ariaLabelledby: "headingFour",
        // },

        {
          title: "Manage number ranges",
          content: "<p>-</p>",
          id: 4,
          idUp: "headingFour",
          ariaExpended: "false",
          dataTarget: "#collapseFour",
          ariaControls: "collapseFour",
          idDown: "collapseFour",
          ariaLabelledby: "headingFour",
        },
        // {
        //   title: "Environmental Samples",
        //   content:
        //     "<p>  <strong>Range: </strong>starts from <strong>1</strong> and ends at <strong>30</strong>. <button> Sample Numbers </button> <button>Export Samples to Excel</button>",
        //   id: 6,
        //   idUp: "headingSix",
        //   ariaExpended: "false",
        //   dataTarget: "#collapseSix",
        //   ariaControls: "collapseSix",
        //   idDown: "collapseSix",
        //   ariaLabelledby: "headingSix",
        // },
        // {
        //   title: "Stratigraphic relationships",
        //   content:
        //   '<button>View All</button> <button> Export Stratigraphic Relationships to Excel </button>',
        //   id: 7,
        //   idUp: "headingSeven",
        //   ariaExpended: "false",
        //   dataTarget: "#collapseSeven",
        //   ariaControls: "collapseSeven",
        //   idDown: "collapseSeven",
        //   ariaLabelledby: "headingSeven",
        // },
        // {
        //   title: "Export Data",
        //   content:
        //   '<button>Export Spot Dates to Excel</button><br><button>Export Photogrammetry to Excel</button><br><button>Export for Deposition</button>',
        //   id: 8,
        //   idUp: "headingEight",
        //   ariaExpended: "false",
        //   dataTarget: "#collapseEight",
        //   ariaControls: "collapseEight",
        //   idDown: "collapseEight",
        //   ariaLabelledby: "headingEight",
        // },
      ],
    };
  },
};
</script>
<template>
  <div>
    <!-- <div id="content" v-html="Content"></div> -->

    <SiteInfoMobile 
    :list="list" class="mobile">MOBILE 
    </SiteInfoMobile>
   <SiteInfoTablet
    :list="list" class="tablet"> TABLET 
    </SiteInfoTablet>
    <SiteInfoDesktop 
    :list="list" class="desktop">DESKTOP
    </SiteInfoDesktop>
  </div>
</template> 
<style>
h6 {
  display: inline-block;
}


body {
  background-color: #f7f7f7 !important;
  /* background-color: #fff !important; */
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
    height: 700px;
   margin: 100px auto;

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
    align-content: center;
    width: 1500px;
    margin-top: 100px;

  }
}
</style>