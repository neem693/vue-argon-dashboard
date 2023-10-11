<template>
    <div id="test" class="container-fluid">
        <div class="row">
            <div class="col-12">
                <span>that component is loading with async</span>
                <TestDefineAsycChild />
            </div>
        </div>
    </div>
</template>
  
<script>
import { onMounted, ref, defineAsyncComponent } from "vue";
const TestDefineAsycChild = defineAsyncComponent(() => import('./components/TestDefineAsycChild'));


export default {
    name: 'TestDefineAsyc',
    components: {
        TestDefineAsycChild
    },
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
  