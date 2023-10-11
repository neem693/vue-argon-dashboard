<template>
  <div id="test" class="container-fluid">
    <div class="row">
      <div class="col-12">
        <span>{{ count }}</span>
      </div>
    </div>
  </div>
</template>

<script>
import { onMounted, ref } from "vue";


export default {
  name: 'Test',
  setup() {
    const count = ref(0);
    onMounted(() => {
      console.log('test')
    })

    function increment() {
      count.value++;
    }

    return {
      count,
      increment
    };
  }
};
</script>
