<script>
    export default { 
        data() {
            return {
                width: '200',
                height: '200',
                myImg: '/assets/me.png'
            }
        },
    }
</script>

<template>
    <!-- add code here -->
    <!-- v-bind:width is the same as :width -->
     <img v-bind:src = "myImg" v-bind:width="width" v-bind:height="height">
     
</template>
