<template>
  <div id="test" class="container-fluid">
    <div class="row">
      <div class="col-12">
        <TestPropsChildOptionApi :message="message1" />
        <TestPropsChildCompositionAPi :message="message2" />
        <TestPropsChildOptionApiDataBinding v-model:message="message3" />
        <TestPropsChildCompositionAPiDataBinding v-model:message="message3" />
      </div>
    </div>
  </div>
</template>

<script>
import { onMounted, ref } from "vue";
import TestPropsChildOptionApi from "./components/TestPropsChildOptionApi.vue";
import TestPropsChildCompositionAPi from "./components/TestPropsChildCompositionAPi.vue";
import TestPropsChildOptionApiDataBinding from "./components/TestPropsChildOptionApiDataBinding.vue";
import TestPropsChildCompositionAPiDataBinding from "./components/TestPropsChildCompositionAPiDataBinding.vue";


export default {
  name: 'TestProps',
  setup() {
    const message1 = ref("message1");
    const message2 = ref("message2");
    const message3 = ref("message3");
    // const count = ref(0);
    onMounted(() => {
      // console.log('test')
    });

    return {
      message1,
      message2,
      message3
    };
  },
  components: { TestPropsChildOptionApi, TestPropsChildCompositionAPi, TestPropsChildOptionApiDataBinding, TestPropsChildCompositionAPiDataBinding }
};
</script>
