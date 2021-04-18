<template>
    <ul>
        <li v-for="(section, index) in sections" :key="index"> <a href="#">{{ section }}</a> </li>
    </ul>
</template>

<script>
export default {
    name: "NavBar",
    data(){
        return {
        sections: ['Section 1', 'Section 2', 'Section 3', 'Section 4']
        }
     }
}
</script>

<style scoped>
ul {
    list-style: none;
    display: flex;
    text-align: center;
    border: solid 1px;
    padding: 10px 20px;
}

li{
    padding: 5px 10px;
    margin-left: auto;
    margin-right: auto;

}
</style>