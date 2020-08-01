<template>
    <div class="list-user">
        <User v-for="user in listUser"
        v-bind:user="user"
              v-bind:key="user.id"
              v-on:deleteUser="deleteUser"
        />
    </div>
</template>

<script>
import User from "./User";
    export default {
        name: "ListUser",
        props: {
            listUser: {
                type: Array
            }
        },
        data(){
            return {
            }
        },
        components: {
            User
        },
        methods: {
            deleteUser(data){
                console.log('list user nhan duoc', data);
                this.$emit('appDeleteUser', data);
            }
        }
    }
</script>

<style scoped>

</style>
