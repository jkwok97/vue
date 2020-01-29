<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <button @click="selectedComp = 'app-quote'">Quote</button>
                <button @click="selectedComp = 'app-author'">Author</button>
                <button @click="selectedComp = 'app-new'">New</button>
                <hr>
                <p>{{ selectedComp }}</p>
                <keep-alive>
                    <component :is="selectedComp"></component>
                </keep-alive>
                <!--<app-quote>
                    <h2 slot="title">{{ quoteTitle }}</h2>
                    <p>A Wonderful Quote!</p>
                    <p>A Wonderful Quote!</p>
                    <p>A Wonderful Quote!</p>
                </app-quote>-->
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    import Author from './components/Author.vue';
    import New from './components/New.vue';

    export default {
        data() {
            return {
                quoteTitle: 'The Quote',
                selectedComp: 'app-quote'
            }
        },
        components: {
            'app-quote': Quote,
            'app-author': Author,
            'app-new': New
        }
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>
