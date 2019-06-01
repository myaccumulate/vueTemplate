<template>
 <div>
   <van-nav-bar  title= "hello" left-arrow @click-left= "onClickLeft" />
 </div>
</template>

<script>
  export default {
    name: 'helloworld',
    data () {
      return {
        
      }
    },
    components: {
      
    },
    methods: {
      onClickLeft () {//返回链接
        this.$router.push('/return');
      },
    },
    watch: {
     
    },
    mounted () {
      this.$axios.post("/u1/area_list")
      .then((data)=>{
        if (data.data.code == 200) {
          // this.$toast("请求成功");
        }
      })
      .catch((err)=>{
      	this.$toast("请求失败");
      	console.log(err);
      })
    }
  }
</script>

<style lang= "stylus">

</style>
