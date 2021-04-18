<template>
<div>
    <div id="header">
        <img src="../assets/logo.png" alt="Logo Vue">
        <ul>
            <li><a href="#">Topic 1</a></li>
            <li><a href="#">Topic 2</a></li>
            <li><a href="#">Topic 3</a></li>
            <li><a href="#">Topic 4</a></li>
        </ul>
        <div id="searchbar">
            <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
            <input type="text" placeholder="Search..">
            <button type="submit"><i class="fa fa-search"></i></button>
        </div>
    </div>
</div>
    

    
</template>

<script>
export default {
    name: "Header",
    
}
</script>

<style scoped>
#header {
    display: flex;
    align-items: center;
}

img{
    margin: 10px;
    width: 80px;
    float: left;

}

ul {
    list-style: none;
    display: flex;
    float: right;
    position: absolute;
    right: 0;
    top: 2px;

}

li{
    padding: 5px 10px;
    border-top: 0;
    right: 10px;
}

#searchbar{
  padding: 6px;
  margin-top: 8px;
  font-size: 17px;
  display: flex;
  position: absolute;
  right: 0;
  top: 60px;
    
}
</style>