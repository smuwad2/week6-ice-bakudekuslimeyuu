<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "demo1" ,
                blueBoth: true 
            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                this.blueBoth =!this.blueBoth 

            }
		}
    }
</script>

<template>
    <!-- vue js help us to connect the HTML script instead of connecting to the DOM -->
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2 " v-bind:class ="{'blueBox': blueBoth, 'redBox': !redBoth}">
            div ID : {{id}} 
        </div>
        <!-- v-onlick short cut is @click -->
        <button type="button" v-bind:class="{'btn btn-primary': blueBoth, 'btn btn-danger': !blueBoth}"
        @click="changeColor()">Change Color</button>

        <!-- <p v-bind:style="{ 'color': 'blue', }"> {{ id }} </p>
        <button v-on:click=changeColor></button> -->

    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
