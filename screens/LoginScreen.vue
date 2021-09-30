<template>
  <view :style="{height:'100%'}" >
      <view :style="{margin:20}">
          <text :style="{fontSize:32,fontWeight:'bold'}">Welcome Back!</text>
          <text :style="{fontSize:15,fontWeight:'bold',color:'grey'}">Log back into your account</text>
      </view>
      <view :style="{marginTop:100,margin:20}">
           <text-input
           class="texti"
        :style="{width: '100%'}"
        placeholder="Your Email"
       
      />
      <text-input
           class="texti"
        :style="{width: '100%',marginTop:30}"
        placeholder="Your Password"
       
      />
      <switch
            :on-value-change="handleChange"
            :trackColor="{ false: '#767577', true: '#81b0ff' }"
            :thumbColor="value ? '#f5dd4b' : '#f4f3f4'"
            :value="value"
            class="sit"
            />
      </view>

      <ImageBackground :source="  require('../assets/login3.jpg')" class="container" resizeMode="cover" :style="{width:'100%',height:'100%',position:'absolute',padding:20,top:'50%'}">

      </ImageBackground>

  </view>
</template>

<script>
export default {
    data(){
        return {
            value: false
        }
    },
methods:{
    handleChange(){
        this.value=!this.value
    }
}
}
</script>

<style>
.texti{
    border-bottom-width: 1px;
    padding-bottom: -20px;
    font-size: 20px;
}
.sit{
    transform: scaleX(0.82),scaleY(1.5);
}
</style>