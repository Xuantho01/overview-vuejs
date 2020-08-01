<template>
    <div class="compo-footer">
        <h1>{{title}}
        </h1>
    </div>
</template>

<script>
    export default {
        name: "CompFooter",
        props: {
            title: {
                type: String,
                default: ' Gia tri dang de mac dinh'
            },
        },
        data(){
            return{

            }
        }
    }
</script>

<style scoped>

</style>
