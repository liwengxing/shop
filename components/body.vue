<template>
    <div cladd='box'>
        <div class='div-warp' v-for='(item,index) in arr' :key='index'>
            <img :src="item.src" alt="">
            <p>{{ item.name }}</p>
            <div class='btndiv'><button @click='jian(index)'>-</button>{{ item.num }}<button @click='add(index)'>+</button></div>
            <div><button class='delbtn' @click='del(index)'>X</button></div>
        </div>
    </div>
</template>

<script>
export default {
    props:['arr'],
    data() {
        return {

        };
    },
    created() {

    },
    mounted() {

    },
    methods: {
        jian(i){
            this.$emit('jian',i)
        },
        add(i){
            this.$emit('add',i)
        },
        del(i){
            this.$emit('del',i)
        }
    }
};
</script>

<style scoped>
html{
    height: 100%;
}
body{
    height: 100%;
}
.box{
    display: flex;
    flex:1;
    width: 100%;
    height: 100%;
}
.div-warp{
    width: 100%;
    height: 50px;
    border: 1px solid #000;
    border-left:none;
    border-right:none;
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.div-warp img{
    width: 50px;
    height: 50px;
}
.btndiv{
    width: 100px;
    height: 30px;
}
.btndiv>button{
    width: 30px;
    height: 30px;
}
.delbtn{
    background-color: rgba(255, 255, 255, 0);
    color: rgb(255, 0, 0);
    font-size:30px;
    border:none;
    outline: none;
}
</style>
