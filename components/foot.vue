<template>
    <div class='footbox'>
        <h2>总结算：{{ num }}</h2>
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
    computed:{
        num(){
            let num=0;
            this.arr.map((item)=>{
                return num+=item.num*item.mary
            })
            return num
        }
    },
    methods: {

    }
};
</script>

<style scoped>
.footbox{
    width: 100%;
    height: 50px;
    background-color: rgb(206, 252, 4);
    display: flex;
    justify-content: space-around;
}
</style>
