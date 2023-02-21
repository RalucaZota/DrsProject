<script>
export default {
  name: "SiteInfoDesktop",

  props: {
    list: Array,
  },
  data() {
    return {
      ids: [1],
      elements: [2, 3, 4],
    };
  },
};
</script>
<template>
  <div class="container">
     <div class="row">
           <div class="accordion" id="accordionExample">
                <div class="col col-lg-4">
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingOne">
                            <button
                                class="accordion-button"
                                type="button"
                                data-bs-toggle="collapse"
                                data-bs-target="#collapseOne"
                                aria-expanded="true"
                                aria-controls="collapseOne"
                            >
                                Project Details
                            </button>
                        </h2>
                            <div
                                id="collapseOne"
                                class="accordion-collapse collapse show"
                                aria-labelledby="headingOne"
                                data-bs-parent="#accordionExample"
                                >
                                <div class="accordion-body">
                                        <ul>
                                        <li>
                                            <strong> Project Name: </strong>Land West of North Ockendon
                                        </li>
                                        <li><strong> Invoice Codes: </strong>LTC40NEV</li>
                                        <li><strong> Cost Center: </strong>OXF</li>
                                        <li><strong> Project Manager: </strong>Steve Lawrence</li>
                                        <li><strong> Start date: </strong>14 Sep 2020</li>
                                        <li>
                                            <strong> Address: </strong> Lower Thames Crossing land west
                                            of North Ockendon land parcels 40 & 49-52
                                        </li>
                                        <li>
                                            <strong> Webmap: </strong
                                            ><span data-v-7c420ce2="" class="mlr-1"
                                            ><a
                                                data-v-7c420ce2=""
                                                href="https://webmap.oxfordarchaeology.com/OCD20"
                                                target="_blank"
                                            >
                                                <button class="button is-info">Click to see the Webmap</button>
                                            </a></span
                                            >
                                        </li>
                                        </ul>
                                  </div>
                            </div>
                    </div>
                    
                </div>

                <div class="col col-lg-4">
                        <div class="accordion-item" v-for="listItem in list" :key="listItem.id" >
                            <h2 class="accordion-header" :id="listItem.idUp">
                                <button
                                class="accordion-button collapsed"
                                type="button"
                                data-bs-toggle="collapse"
                                :data-bs-target="listItem.dataTarget"
                                :aria-expanded="listItem.ariaExpended"
                                :aria-controls="listItem.ariaControls"
                                >
                                {{ listItem.title }}
                                </button>
                            </h2>

                                <div
                                    :id="listItem.idDown"
                                    :class="
                                    ids.includes(listItem.id)
                                        ? 'accordion-collapse collapse show'
                                        : 'accordion-collapse collapse'
                                    "
                                    :aria-labelledby="listItem.ariaLabelledby"
                                    data-bs-parent="#accordionExample"
                                >
                                    <div class="accordion-body"  
                                    :class="
                                elements.includes(listItem.id)
                                ? 'reduce-dimen'
                                : ''">
                                    <span v-html="listItem.content"></span>
                                    </div>
                                </div>
                        </div>
                </div>

                <div class="col-lg-4">
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingFive">
                        <button
                            class="accordion-button collapsed"
                            type="button"
                            data-bs-toggle="collapse"
                            data-bs-target="#collapseFive"
                            aria-expanded="false"
                            aria-controls="collapseFive"
                        >
                            Trenches
                        </button>
                        </h2>
                         <div
                            id="collapseFive"
                            class="accordion-collapse collapse"
                            aria-labelledby="headingFive"
                            data-bs-parent="#accordionExample"
                            >
                            <div class="accordion-body">
                                <ul>
                                <li>
                                    <strong> <button class="button is-info">View Report</button></strong>
                                </li>
                                <li>
                                    <strong>
                                    <button class="button is-info">
                                        Trenches Register
                                    </button></strong
                                    >
                                </li>
                                <li><strong> Number of thrences: </strong>144</li>
                                <li>
                                    <strong>
                                    <button class="button is-info">
                                        Context Numbers
                                    </button></strong
                                    >
                                </li>
                                <li>
                                    <strong>
                                    <button class="button is-info">
                                        Export Contexts to Excel
                                    </button></strong
                                    >
                                </li>
                                <li>
                                    <strong>
                                    <button class="button is-info">
                                        Export Trench Tables to Excel
                                    </button></strong
                                    >
                                </li>
                                <li>
                                    <strong>
                                    <button class="button is-info">
                                        Export Trench Register to Excel
                                    </button></strong
                                    >
                                </li>
                                </ul>
                            </div>
                        </div>
                    </div>

               </div>



               <div class="col col-lg-4">
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingSix">
                        <button
                            class="accordion-button collapsed"
                            type="button"
                            data-bs-toggle="collapse"
                            data-bs-target="#collapseSix"
                            aria-expanded="false"
                            aria-controls="collapseSix"
                        >
                            Environmental Samples
                        </button>
                        </h2>
                        <div
                        id="collapseSix"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingSix"
                        data-bs-parent="#accordionExample"
                        >
                            <div class="accordion-body">
                                <ul>
                                <li>
                                    <h3>Environmental Samples</h3>
                                </li>
                                </ul>
                                <ul>
                                <li>
                                    <strong>Range: </strong>starts from <strong>1</strong> and
                                    ends at <strong>30</strong>.
                                </li>
                                <li>
                                    <strong>
                                    <button class="button is-info">
                                        Sample Numbers
                                    </button></strong
                                    >
                                </li>
                                <li>
                                    <strong>
                                    <button class="button is-info">
                                        Export Samples to Excel
                                    </button></strong
                                    >
                                </li>
                                </ul>
                            </div>
                        </div>
                    </div>

               </div>
               <div class="col col-lg-4">
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingSeven">
                        <button
                            class="accordion-button collapsed"
                            type="button"
                            data-bs-toggle="collapse"
                            data-bs-target="#collapseSeven"
                            aria-expanded="false"
                            aria-controls="collapseSeven"
                        >
                            Stratigraphic Relationships
                        </button>
                        </h2>
                        <div
                        id="collapseSeven"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingSeven"
                        data-bs-parent="#accordionExample"
                        >
                            <div class="accordion-body">
                                
                                <ul>
                                <li>
                                     <button class="button is-info">View All</button>
                                </li>
                                <li>
                                    <button class="button is-info">
                                        Export Stratigraphic Relationships to Excel
                                    </button>
                                </li>
                              
                                </ul>
                            </div>
                        </div>
                    </div>

               </div>

               <div class="col col-lg-4">
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingEight">
                        <button
                            class="accordion-button collapsed"
                            type="button"
                            data-bs-toggle="collapse"
                            data-bs-target="#collapseEight"
                            aria-expanded="false"
                            aria-controls="collapseEight"
                        >
                            Export Data
                        </button>
                        </h2>
                        <div
                        id="collapseEight"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingEight"
                        data-bs-parent="#accordionExample"
                        >
                            <div class="accordion-body">
                                
                                <ul>
                                <li>
                                       <button class="button is-info">
                                            Export Spot Dates to Excel
                                        </button>
                                </li>
                                <li>
                                        <button class="button is-info">
                                                    Export Photogrammetry to Excel
                                        </button>
                                </li>
                                <li>
                             
                                <button class="button is-info">
                                    Export for Deposition
                                </button>
                                
                                </li>
                              
                                </ul>
                            </div>
                        </div>
                    </div>

               </div>


          </div>
     </div>
  </div>
</template>

<style>
.accordion .accordion-item .accordion-button {
  border: 5px solid #5d3f6a;

  background-color: #f7f7f7;

  border-radius: 5px;

  color: black;

  font-weight: 700;
}

.accordion-item:last-of-type .accordion-button.collapsed {
  border-radius: 5px;
}

.accordion-body {
  background-color: #f7f7f7;

  border: 1px solid gray;

  border-radius: 5px;
}

@media screen and (min-width: 1200px) {
  .accordion-body {
    height: 270px;
  }

  .button-class {
    background-color: #5d3f6a;
  }

  .accordion-item.accordion-collpase.collapse {
    background-color: pink;
    margin: 20px;
  }

  .accordion-button.collapse {
    margin-bottom: 50px;
  }

  .accordion.accordion-item {
    background-color: #f7f7f7;
    border: #f7f7f7;
  }
  li {
    list-style: none;
    margin-left: -30px;
  }

  .dimension {
    height: 130px;
  }
  .reduce-dimen {
    height: 100px;
  }
  .button.is-info {
    border: 3px solid #5d3f6a;
    margin-bottom: 5px;
    border-radius: 5px;
  }
}
</style>
