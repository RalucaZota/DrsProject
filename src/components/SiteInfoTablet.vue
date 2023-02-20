<script>
export default {
  name: "SiteInfoTablet",
  props: {
    List: Array,
  },
  data() {
    return {
      id1: 1,
      id2: 2,
    };
  },
};
</script>
<template>
  <div>
      <div class="accordion" id="accordionExample" v-for="listItem in List" :key="listItem.id">
        <div class="accordion-item">
          <h2 class="accordion-header" :id="[listItem.idUp]">
            <button
              class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
              :data-bs-target="[listItem.dataTarget]"

              :aria-expanded="[listItem.ariaExpended]"
              :aria-controls="[listItem.ariaControls]"
            >
              {{ listItem.Title }}
            </button>
          </h2>
          <div
            :id="[listItem.idDown]"
            class="accordion-collapse collapse"  :class="{'show' : listItem.id === id1 || listItem.id === id2}"
        
            :aria-labelledby="[listItem.ariaLabelledby]"
            data-bs-parent="#accordionExample"
            style=""
          >
            <div class="accordion-body" >
              <span v-html="listItem.Content"></span>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>
<style>
.accordion .accordion-item .accordion-button {
  /* border: 5px solid #0f402f;  */
  border: 5px solid #5d3f6a;
  background-color: #f7f7f7;
  border-radius: 5px;
  color: black;
  font-weight: 700;
}

.accordion-button.collpased {
  border: 3px solid greenyellow;
}
.accordion-item:first-of-type .accordion-button {
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
.accordion-item:last-of-type .accordion-button.collapsed {
  border-radius: 5px;
  border-bottom-right-radius: 5px;
  border-bottom-left-radius: 5px;
}

.accordion-item:first-of-type .accordion-button {
}
.accordion-button:not(.collapsed) {
  background-color: #961818;
}
.accordion-body {
  background-color: #f7f7f7;
  border: 1px solid gray;
  border-radius: 5px;
  height: 230px;
}

</style>
