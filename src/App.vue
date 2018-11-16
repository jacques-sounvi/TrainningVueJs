<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <button @click="selectComponent = 'appQuote' ">Quote</button>
                <button @click="selectComponent = 'appAuthor' ">Author</button>
                <button @click="selectComponent = 'appNew' ">New</button>
                <hr>
                <p>{{selectComponent}}</p>
                <component :is="selectComponent" >
                    <p>Default</p>
                </component>
                <!-- <app-quote>
                    <h2 slot="title">{{quoteTitle}}</h2>
                    <p slot="subtitile"></p>
                    <p>A wonder Quote</p>
                </app-quote> -->
               
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue'
    import Author from './components/Author.vue'
    import New from './components/New.vue'

    export default {

        data(){
            return{
                quoteTitle: "The Quote",
                selectComponent: "appQuote"
            };
        },
        components: {
            appQuote: Quote,
            appAuthor: Author,
            appNew: New
        }
    }
</script>

<style>
</style>
