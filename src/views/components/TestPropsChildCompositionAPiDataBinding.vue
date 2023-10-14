<template>
  <div id="test" class="container-fluid">
    <div class="row">
      <div class="col-12">
        <span>22 - {{ message }}</span>
        <button @click="buttonClick($event)">button click</button>
      </div>
    </div>
  </div>
</template>

<script>
import {
  // toRefs,  
  onMounted
} from 'vue';
export default {
  name: 'TestPropsChildCompositionAPiDataBinding',
  data: () => ({
    messageHere: '',

  }),
  props: {
    message: {
      type: [String],
      required: true
    }
  },
  setup(_, { emit }) {

    // const { message } = toRefs(props)
    // console.log('')
    onMounted(() => {
      // console.log('TestPropsChildCompositionAPiDataBinding', refs, refs.value, modelValue.value)
    })

    const buttonClick = (event) => {
      console.log(event)
      emit('update:message', "message_composition_api")
    }

    return {
      buttonClick
      // message
    }
  }


};
</script>
