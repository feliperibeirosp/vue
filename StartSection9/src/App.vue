<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button @click="selectedComponent='appBlue'" class="btn btn-primary">Asa Akira</button>
                <button @click="selectedComponent='appGreen'" class="btn btn-success">Mia Khalifa</button>
                <button @click="selectedComponent='appRed'" class="btn btn-danger">Sasha Grey</button>
                <hr>
                <component :is="selectedComponent">
                </component>
               <!-- <app-blue></app-blue>
                <app-green></app-green>
                <app-red></app-red>
                -->
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        data: function() {
            return {
                selectedComponent: 'appBlue'
            }
        },
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>
</style>
