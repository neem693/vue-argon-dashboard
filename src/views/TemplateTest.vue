<template>
    <div id="test" class="container-fluid">
        <div class="row">
            <div class="col-12">
                <TemplateChild>
                    <template #child1>
                        <p>hohohoho child1</p>
                    </template>
                    <template #child2>
                        <p>hohohoho child2</p>
                    </template>
                </TemplateChild>
            </div>
        </div>
    </div>
</template>
  
<script>
import { onMounted } from "vue";
import TemplateChild from "./components/TemplateChild.vue";


export default {
    name: 'TemplateTest',
    setup() {
        onMounted(() => {
            console.log('template test');
        });
    },
    components: { TemplateChild }
};
</script>
  