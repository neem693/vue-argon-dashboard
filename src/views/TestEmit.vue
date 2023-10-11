<template>
    <div id="test" class="container-fluid">
        <div class="row">
            <div class="col-12">val : {{ val }}</div>
            <div class="col-12">
                <TestEmitChild @trigger="setVal"></TestEmitChild>
            </div>
            <div class="col-12">
                <TestEmitChild2 @trigger="setVal"></TestEmitChild2>
            </div>
        </div>
    </div>
</template>
  
<script>

import TestEmitChild from "./components/TestEmitChild.vue";
import TestEmitChild2 from "./components/TestEmitChild2.vue";
import { ref, onMounted } from "vue";
export default {
    name: 'TestEmit',
    components: {
        TestEmitChild,
        TestEmitChild2
    },
    setup() {

        const val = ref("init")
        const setVal = (data) => {
            console.log('data', data)
            val.value = data
        }
        const setVal2 = (data) => {
            console.log('data', data)
            val.value = data
        }

        onMounted(() => {
            console.log('val', val.value)
            // val.value = 'init'
        })

        return {
            setVal,
            setVal2,
            val
        }
    }
};
</script>
  