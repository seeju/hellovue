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
        sections: ['Section 1', 'Section 2', 'Section 3', 'Section 4', 'Section 5', 'Section 6', 'Section 7', 'Section 8', 'Section 9', 'Section 10', 'Section 11', 'Section 12', 'Section 13', 'Section 14', 'Section 15']
        }
     }
}
</script>

<style scoped>
ul {
    height: 100%; 
    width: 160px; 
    position: absolute; 
    right: 0;
    overflow-x: hidden; 
    padding-top: 20px;
    margin-top: auto;
    margin-bottom: auto;
    list-style: none;

}

li{
    padding: 5px 10px;
    margin-left: auto;
    margin-right: auto;

}
</style>