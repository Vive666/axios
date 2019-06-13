<template>
    <div class="a">
      
         <table>
             <tr>
                 <td>id</td>
                 <td>IMEI</td>
                 <td>device</td>
                 <td>message</td>
                 <td>tel</td>
             </tr>
            <tr v-for="index in syk" :key="index">
                <td>{{index.id}}</td>
                <td>{{index.IMEI}}</td>
                <td>{{index.device}}</td>
                <td>{{index.message}}</td>
                <td>{{index.tel}}</td>
            </tr>
         </table>
         <button @click="danji">你点我我就出来</button>
      
    </div>
</template>

<script>

export default {
  data(){
    return{
      syk:'',
    }
  },
  methods:{
    danji:function () {
     
    this.axios.get('http://localhost:60020/all').then((response)=>{
    console.log(response.data);
    this.syk=response.data.data;
    console.log(this.syk);
    }).catch((error)=>{
        console.log(error)
    })
},
    }
  
  
  // METHODS:{
  //     danji:function(){
  //       alert("1")
  //     }
  // }
}
</script>
<style>
table{
    table-layout:fixed;
    empty-cells:show; 
    border-collapse: collapse;
    margin:0 auto;
    border: 2px solid black
}
td{
    border: 1px solid black;
    height:20px;
}
</style>

