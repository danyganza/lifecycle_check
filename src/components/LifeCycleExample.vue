<template>
    <div>
<h1>hello</h1>
    </div>
</template>

<script>
    export default {
        beforeCreate: function (){
            console.log(`hello`)
        },
        created: function (){
            console.log(`hello there`)
        },
        beforeMount: function (){
            console.log(`hello hi`)
        },
        mounted : function (){
            console.log(`hell hello`)
        }
    }
</script>

<style scoped>

</style>