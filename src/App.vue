<template>
  <div id="app">
      <!-- <p>{{syk}}</p> -->
      <list />
    <router-view/>
  </div>
</template>

<script>
import list from './components/list.vue'
export default {
  components:{
    list
  }
  // data(){
  //   return{
  //     syk:'1dd23',
  //   }
  // },
//   created(){
//     this.axios.get(api).then((response) => {
//   console.log(response.data)
// })

//   }

    //   created(){
    //   this.axios.get('http://localhost:60020/all').then((response)=>{
    //     console.log(response.data.data[1]);
    //     this.syk=response.data.data;
    //     console.log(this.syk);
    //   }).catch((error)=>{
    //       console.log(error)
    //   })
    // }
    

}
</script>

<style>

</style>
