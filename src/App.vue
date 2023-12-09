<script>
import {ref} from 'vue'
export default{
  setup(){
    const datas=ref([])
    const getData=async function(){
      const datafecth= await fetch('http://localhost:3000/posts')
      const response=datafecth.response()
      const convert=response.json()
      console.log(convert)
    }
    return{datas,getData}
  },
  mounted(){
    this.getData()
  }
}
</script>

<template>

</template>