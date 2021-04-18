<template>
    <div>
        <article v-for="(item,index) in items" :key="index">
            <img v-bind:src="item.link" v-bind:alt="item.title">
            <p>{{ item.content }}</p>
        </article>
    </div>


</template>

<script>

export default {
    name:"Article",

    data(){
        return {
        items: [
            {   id: 0,
                content: 'Duis dolor fugiat excepteur labore reprehenderit occaecat excepteur. Do ut labore adipisicing ut. Ad minim quis ea aliquip non ea. Duis ad quis culpa consectetur minim aliquip in cupidatat qui consectetur aliqua dolor nulla incididunt. Laborum reprehenderit veniam nisi consectetur est mollit fugiat voluptate amet ea incididunt esse. Nulla fugiat ea proident amet.',
                link: 'data:image/jpeg;base64,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',
                title: 'Black Cat one'
            },
            {   id: 1,
                content: 'Duis dolor fugiat excepteur labore reprehenderit occaecat excepteur. Do ut labore adipisicing ut. Ad minim quis ea aliquip non ea. Duis ad quis culpa consectetur minim aliquip in cupidatat qui consectetur aliqua dolor nulla incididunt. Laborum reprehenderit veniam nisi consectetur est mollit fugiat voluptate amet ea incididunt esse. Nulla fugiat ea proident amet.',
                link: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTR9sM6H8qyUMwkfe01Enx-JkzAwkcpZ5L9sw&usqp=CAU',
                title: 'Black Cat two'
            },
            {   id: 2,
                content: 'Duis dolor fugiat excepteur labore reprehenderit occaecat excepteur. Do ut labore adipisicing ut. Ad minim quis ea aliquip non ea. Duis ad quis culpa consectetur minim aliquip in cupidatat qui consectetur aliqua dolor nulla incididunt. Laborum reprehenderit veniam nisi consectetur est mollit fugiat voluptate amet ea incididunt esse. Nulla fugiat ea proident amet.',
                link: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTRN5UyEy5hG8tJJpJQirvHaDM9bEgrB2UXDw&usqp=CAU',
                title: 'Black Cat three'
            }
            ]
        }
     }
    
}
</script>

<style scoped>
img {
    display: flex;
    float: left;
    width: 200px;
    height: 120px;
}

article{
    float: left;
    display: flex;
}

img {
    display: flex;
    width: 200px;
    height: 150px;

}

p {

    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 20px;
    margin-right: 200px ;
}
</style>