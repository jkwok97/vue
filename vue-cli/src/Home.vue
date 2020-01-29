<template>
    <div>
        <app-server-status v-for="(server, index) in 5" :key="index"></app-server-status>
    </div>
</template>

<script>
    import serverStatus from './ServerStatus.vue'
    export default {
        components: {
            'app-server-status': serverStatus 
        }
    }
</script>