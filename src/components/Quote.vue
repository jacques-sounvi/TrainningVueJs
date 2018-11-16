<template>
    <div>
       <div class="title">
           <slot name="title"></slot>
       </div>
       <hr>
       <div>
           <slot name="content"></slot>
       </div>
    </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
    div{
        border: 1px solid #cccccc;
        box-shadow: 1px 1px 2px black;
        padding: 30px;
        text-align: center;
    }
    h2{
        color:red
    }
</style>