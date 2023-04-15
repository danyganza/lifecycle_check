<template>
    <div>
<h1>hello, this is cool</h1>
<h3>I kinda like it</h3>
    </div>
</template>

<script>
    export default {
        beforeCreate: function (){
            console.log(`hello from the other side`)
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