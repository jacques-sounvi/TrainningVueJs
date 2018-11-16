<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User Name : {{swithName()}} </p>
        <p>User Age: {{userAge}}</p>
         <button @click="ResetName">Reset name</button>

    </div>
</template>

<script>
    export default{
        props: {
            myName:{
                type: String
            },
            userAge: Number
        },
        methods:{
            swithName(){
                return this.myName.split("").reverse().join("");
            },
            ResetName(){
                this.myName = 'Max'
                 this.$emit('nameWasReset',this.myName);
            }
        }
    }
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
