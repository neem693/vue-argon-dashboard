<template>
    <div id="test" class="container-fluid">
        <div class="row">
            <div class="col-12">
                <slot name="child1"></slot>
            </div>
        </div>
        <div class="row">
            <div class="col-12">
                <p>////////////////////</p>
            </div>
        </div>
        <div class="row">
            <div class="col-12">
                <slot name="child2"></slot>
            </div>
        </div>
    </div>
</template>
  
<script>
import { onMounted, ref } from "vue";


export default {
    name: 'TemplateChild',
    setup() {
        const count = ref(0)
        onMounted(() => {
            console.log('count', count)
            console.log('Template child vue')
        })



    }
};
</script>
  