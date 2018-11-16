<template>
    <div class="component">
        <h1>The User Component</h1>
        <p>I'm an awesome {{name}}</p>
        <button @click="ChangeName">Change name</button>
        <p>{{name}}</p>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <app-user-detail :myName="name" @nameWasReset="name = $event"></app-user-detail>
            </div>
            <div class="col-xs-12 col-sm-6">
                <app-user-edit></app-user-edit>
            </div>
        </div>
    </div>
</template>

<script>
    import UserDetail from './UserDetail.vue';
    import UserEdit from './UserEdit.vue';

    export default {
        components: {
            appUserDetail: UserDetail,
            appUserEdit: UserEdit
        },
         data(){
           return{
               name: 'max'
           };
       },
       methods:{
           ChangeName(){
               this.name = 'Anna'
           }

       }
    }
</script>

<style scoped>
    div {
        background-color: lightblue;
    }
</style>
