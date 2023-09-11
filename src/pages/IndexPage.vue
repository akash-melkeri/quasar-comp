<template>
  <q-page class="">
    <CollectionButtons
      v-if="
        $route.query.component == 'buttons' ||
        Object.keys($route.query).length == 0
      "
    ></CollectionButtons>
    <CollectionTextInputs
      v-if="$route.query.component == 'text-inputs'"
    ></CollectionTextInputs>
    <CollectionFileInputs
      v-if="$route.query.component == 'file-inputs'"
    ></CollectionFileInputs>
    <CollectionTextarea
      v-if="$route.query.component == 'textareas'"
    ></CollectionTextarea>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import CollectionButtons from "src/components/CollectionButtons.vue";
import CollectionTextInputs from "src/components/CollectionTextInputs.vue";
import CollectionFileInputs from "src/components/CollectionFileInputs.vue";
import CollectionTextarea from "src/components/CollectionTextarea.vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    CollectionButtons,
    CollectionTextInputs,
    CollectionFileInputs,
    CollectionTextarea
  },
  setup() {
    return {
      map: {
        buttons: {}
      }
    };
  }
});
</script>
