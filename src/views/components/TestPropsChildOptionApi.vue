<template>
  <div id="test" class="container-fluid">
    <div class="row">
      <div class="col-12">
        <span>{{ message }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TestPropsChildOptionApi',
  data: () => ({
    messageHere: '',

  }),
  props: {
    message: {
      type: [String],
      required: true
    }
  },
  mounted() {

  },

};
</script>
