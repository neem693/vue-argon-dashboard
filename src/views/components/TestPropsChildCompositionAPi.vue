<template>
  <div id="test" class="container-fluid">
    <div class="row">
      <div class="col-12">
        <span>{{ message }}</span>
        <span>//{{ messageLocal }}</span>

      </div>
    </div>
  </div>
</template>

<script>
import { onMounted, ref, watch, toRefs } from 'vue';

export default {
  name: 'TestPropsChildCompositionAPi',
  props: {
    message: {
      type: [String],
      required: true
    }
  },
  setup(props) {

    const { message } = toRefs(props)
    const messageLocal = ref("message_")

    onMounted(() => {


    })

    watch(message, (newVal, oldVal) => {
      console.log(newVal, oldVal)
      if (newVal === "message2") {
        messageLocal.value = "message_local"
      }
    });

    return {
      messageLocal
    }
  }

};
</script>
