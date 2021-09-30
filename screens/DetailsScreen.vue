<template>

    <ImageBackground :source="  require('../assets/content.jpg')" class="container" resizeMode="cover" :style="{width:'100%',height:'100%',position:'relative',padding:20}">
      <view :style="{}">
           <text class="" :style="{fontSize:39,fontWeight:'bold'}">HomeCraft</text>
        <text class="text-color-primary">Modern Furniture and decor for your home</text>
      </view>

      
            <view class="btn">
             <TouchableOpacity
             :activeOpacity="0.9"
             :onPress="goToLogin"
        class="r-btn"
        
      >
        <Text :style="{fontWeight:'bold',fontSize:17}">Start Shopping</Text>
      </TouchableOpacity>
       
       </view>
    </ImageBackground>
  

</template>

<script>
import {BackHandler,Alert, ImageBackground,button } from 'react-native'


export default {
     props: {
    navigation: {
      type: Object
    }
  },
  data(){
      return {
        
      }
  },
  methods:{
       backAction ()  {
      
          Alert.alert("Hold on!", "Are you sure you want to go Exit?", [
        {
          text: "Cancel",
          onPress: () => null,
          style: "cancel"
        },
        { text: "YES", onPress: () => BackHandler.exitApp() }
      ]);
      return true;
      
    },
      goToLogin(){
        this.navigation.navigate('Login')
      }
  },
  created(){
    
    // if(this.navigation.state.routeName=="Home"){
    //   BackHandler.addEventListener(
    //   "hardwareBackPress",
    //   this.backAction()
      
    // );
    
    // }else{
    //   BackHandler.removeEventListener("hardwareBackPress", this.backAction());
    // }
  },
  beforeDestroy(){
    // BackHandler.removeEventListener("hardwareBackPress", this.backAction());
  },
 
}
</script>

<style>
.container {
  background-color: white;
  align-items: flex-start;
  /* justify-content: center; */
  flex: 1;
  width: '100%';
 
}
.text-color-primary {
  color: #96959A;
  font-size: 15px;
  width: 212px;
  font-weight: bold;
}
.btn{
    position: absolute;
    bottom:50px;
    width: 100%;
    margin: 20px;
    
    
}
.r-btn{
    width: 100%;
   
    color: black;
    background-color: #FED07A;
     align-items: center;
     padding: 11;
     height: 50px;
}
</style>