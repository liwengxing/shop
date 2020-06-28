<template>
  <div id="app">
  <Headcont></Headcont>
  <Bodycont class='Bodycont' :arr='bodyArr' @jian='jian' @add='add' @del='del'></Bodycont>
  <footcont :arr='bodyArr'></footcont>
  </div>
  
</template>

<script>
import Headcont from './components/head'
import Bodycont from './components/body'
import footcont from './components/foot'
export default {
  name: 'App',
 
  data(){
    return{
      bodyArr:[
        {name:'苹果X', src:'https://dss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3661752605,810466684&fm=26&gp=0.jpg',mary:1000,num:1},
        {name:'苹果ipaX', src:'https://dss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3273224725,2245233908&fm=26&gp=0.jpg',mary:1500,num:1},
        {name:'苹果电脑X', src:'https://dss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=380614410,1284333573&fm=26&gp=0.jpg',mary:2000,num:1},
        {name:'华为', src:'https://dss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=2328910668,2191196265&fm=26&gp=0.jpg',mary:2500,num:1},
        {name:'vivo', src:'https://dss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=2929430211,72684005&fm=26&gp=0.jpg',mary:3000,num:1},
        {name:'笔记本', src:'https://dss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3791988138,2770084496&fm=26&gp=0.jpg',mary:3500,num:1},
      ]
    }
  },
  
  methods:{
   jian(i){
     this.bodyArr[i].num--
       if(this.bodyArr[i].num==0){
           this.bodyArr.splice(i,1)
        }
   },
   add(i){
     this.bodyArr[i].num++
   },
   del(i){
            this.bodyArr.splice(i,1)
        }
  },
  components:{
   Headcont,Bodycont,footcont
  }
}

</script>

<style>
html{
  height: 100%;
}
body{
  height: 100%;
}
*{
    margin:0;
    padding:0;
}
#app {
 width: 100%;
 height: 100%;
 display:flex;
 flex-direction: column;
 /* justify-content: space-between; */
}
.Bodycont{
  flex:1;
}
</style>
