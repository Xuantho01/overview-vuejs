<template>
    <div class="user">
        <p>
            {{user.email}}
            <button
            v-on:click="deleteUser"
            >
                delete
            </button>
        </p>
    </div>
</template>

<script>
    export default {
        name: "User",
        props: {
            user: Object
        },
        data() {
            return{
            }
        },
        methods: {
            deleteUser(){
               var data = {
                   id: this.user.id
                };
                console.log("user gui yeu cau delete user");
               this.$emit('deleteUser', data);

            }
        }
    }
</script>

<style scoped>

</style>
