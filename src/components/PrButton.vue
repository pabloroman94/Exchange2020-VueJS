<template>
    <button
    @click="buttonClick"
     class="bg-transparent hover:bg-green-500 text-green-700font-semibold hover:text-white py-2 px-2 borderborder-green-500 hover:border-transparent rounded
">
<beat-loader :loading="isLoading" :color="'#98b391'" :size="8" />
<p v-show="!isLoading">
    <slot></slot>
</p>
</button>
</template>

<script>
export default {
    name:'PrButton',
    props:{
        isLoading:{
            type: Boolean,
            default: false
        }
    },
    methods:{
        buttonClick(){
            this.$emit('custom-click')
        }
    }
}
</script>