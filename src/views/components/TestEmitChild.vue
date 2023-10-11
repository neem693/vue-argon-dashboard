<template>
    <div id="test" class="container-fluid">
        <div class="row">
            <div class="col-12">
                <div class="col-6 text-end">
                    <button @click="trigger()" color="dark" variant="gradient">
                        <i class="fas fa-plus me-2"></i>
                        OptionApi(check)
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>


export default {
    name: 'TestEmitChild',
    data: () => {
        return {}
    },
    emits: ['trigger'],
    mounted() {

    },
    methods: {
        trigger() {
            this.$emit('trigger', 'check')
        }
    }
};
</script>
  