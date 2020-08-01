<template>
    <div class="comp-tabs">
    <div class="comp-title">
            <p>{{title}}</p>
    </div>
    <div class="tabs-content">
        <slot>
        </slot>
    </div>
    </div>
</template>

<script>
    export default {
        name: "compTabs",
        props: {
            title: String
        },
        data(){
            return{

            }
        }
    }
</script>

<style scoped>

</style>
