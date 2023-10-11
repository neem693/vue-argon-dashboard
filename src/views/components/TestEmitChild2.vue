<template>
    <div id="test" class="container-fluid">
        <div class="row">
            <div class="col-12">
                <div class="col-6 text-end">
                    <button @click="trigger()" color="dark" variant="gradient">
                        <i class="fas fa-plus me-2"></i>
                        composition API(check2)
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>

// import { defineEmits } from "vue";
export default {
    name: 'TestEmitChild2',
    setup(_, { emit }) {

        // const emit = defineEmits(['trigger'])
        const trigger = () => {
            emit('trigger', 'check2')
        }

        return {
            trigger
        }
    }
};
</script>
  