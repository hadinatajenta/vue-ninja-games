<template lang="">
    <div class="block" v-if="showBlock">
        Click me
    </div>
</template>
<script>
export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false
        }
    },
    mounted(){
        setTimeout(()=> {
            this.showBlock = true
            console.log(this.delay)
        }, this.delay)
    },
    updated(){
        console.log('component updated')
    },
    unmounted(){
        console.log('unmounted')
    }
}
</script>
<style >
    .block{
        width: 400px ;
        border-radius: 20px;
        background-color: red;
        color: white;
        text-align: center;
        padding: 100px 0;
        margin: 40px auto;
    }
</style>