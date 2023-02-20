<script>
export default {
  name: "Card",
  props: {
      List: Array,
    },
};
</script>
<template>
    <div>

  <div class="accordion" >
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
        
          <!-- <h3>Project Details</h3> -->
          <slot name="Title" ></slot>
        </button>
      </h2>
      <div
        id="collapseOne"
        class="accordion-collapse collapse" :class="{'show' : id === 1}"
        aria-labelledby="headingOne"
        data-bs-parent="#accordionExample"
      >
        <div class="accordion-body">
            <slot name="Content" >

            </slot>
          <!-- <ul>
            <li><strong> Project Name: </strong>Land West of North Ockendon</li>
            <li><strong> Invoice Codes: </strong>LTC40NEV</li>
            <li><strong> Cost Center: </strong>OXF</li>
            <li><strong> Project Manager: </strong>Steve Lawrence</li>
            <li><strong> Start date: </strong>14 Sep 2020</li>
            <li>
              <strong> Address: </strong> Lower Thames Crossing land west of
              North Ockendon land parcels 40 & 49-52
            </li>
            <li>
              <strong> Webmap: </strong
              ><span data-v-7c420ce2="" class="mlr-1"
                ><a
                  data-v-7c420ce2=""
                  href="https://webmap.oxfordarchaeology.com/OCD20"
                  target="_blank"
                >
                  <button class="button is-info">
                    Click to see the Webmap
                  </button>
                </a></span
              >
            </li>
          </ul> -->
        </div>
      </div>
    </div>
  </div>
</div>
</template>
