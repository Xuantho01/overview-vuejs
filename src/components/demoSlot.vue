<template>
    <div class="demo-slot">
        <CompTabs title="tieu de cua tab">
            <ul class="tabs-header">
                <li v-for ="(item, index) in tabsHeader"
                v-bind:key="index"
                v-on:click="changActive(index)">{{ item.text}}</li>
            </ul>
        <div class="tab-content tab1" v-if="tabActice === 0">
            <p> day la tab 1</p>
        </div>
            <div class="tab-content tab2" v-else-if="tabActice === 1">
                <p> day la tab 2</p>
            </div>
            <div class="tab-content tab3"  v-else>
                <p> day la tab 3</p>
            </div>
        </CompTabs>
    </div>
</template>

<script>
    import CompTabs from "./compTabs";
    export default {
        name: "demoSlot",
        components: {
        CompTabs
        },
        data(){
            return{
                tabsHeader: [
                    {text: 'Tab1'},
                    {text: 'Tab2'},
                    {text: 'Tab3'}
                ],
                tabActice: 0
            }
        },
        methods: {
            changActive(index){
                this.tabActice = index;
            }
        }
    }
</script>

<style scoped>

</style>
