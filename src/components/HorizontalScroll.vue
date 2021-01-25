<template>
    <div class="_horizontal-scroll">
        <slot></slot>
    </div>
</template>

<script>
export default {
    mounted() {
        const content = this.$el;
        //Firefox
        if(content.addEventListener){
            content.addEventListener('wheel', function(e){
            content.scrollBy(e.deltaY * 20, 0);
            }, false);
        }

        //IE
        if(content.attachEvent){
            content.attachEvent('onmousewheel', function(e){
            content.scrollBy(-e.wheelDelta, 0);
            });
        }

        //Chrome
        content.onmousewheel = function(e){
            content.scrollBy(-e.wheelDelta, 0);
        }
    }
}
</script>

<style scoped>
._horizontal-scroll {
    box-sizing: border-box;
    overflow-x: scroll;
    overflow-y: hidden;
    text-align: left;
    white-space: nowrap;
}
</style>
