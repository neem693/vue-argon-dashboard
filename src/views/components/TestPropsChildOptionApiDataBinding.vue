<template>
  <div id="test" class="container-fluid">
    <div class="row">
      <div class="col-12">
        <span>11 - {{ message }}</span>
        <button @click="buttonClick($event)">button click</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TestPropsChildOptionApiDataBinding',
  data: () => ({
    messageHere: '',

  }),
  props: {
    message: {
      type: [String],
      required: true,
    }
  },
  emits: ["update:message"],
  mounted() {
    console.log('value', this.message)
    // this.$emit('update:value', newValue);
  },
  watch: {
    value(newVal, oldVal) {
      console.log(newVal, oldVal)
    }
  },
  methods: {
    buttonClick: function (event) {
      console.log('button click', event)
      this.$emit('update:message', 'message_option_api')
    }
  }

};
</script>
