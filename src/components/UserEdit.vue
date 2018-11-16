<template>
    <div class="component">
        <h3>You may edit the User here</h3>
        <p>User age: {{userAge}}</p>
        <button @click="editAge">Edit me </button>
    </div>
</template>

<script>
    export default{
        props:['userAge'],
        methods:{
            editAge(){
                this.userAge = 30
                this.$emit('ageWasChanged',this.userAge)
            }
        }
    }
</script>

<style scoped>
    div {
        background-color: lightgreen;
    }
</style>
