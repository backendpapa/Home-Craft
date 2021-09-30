<template>
  <view class="container">
      <view>
        <StatusBar
        :animated="true"
        backgroundColor="#ECEEF0"
        
        
        />
                  <image :style="{width: 80, height: 140}"
          :source="require('../assets/chair.png')"
        />
      </view>
    <text class="" :style="{fontSize:30,fontWeight:'bold'}">HomeCraft</text>
</view>
</template>

<script>
export default {
    props: {
    navigation: {
      type: Object
    }
  },
  
  methods: {
    goToHomeScreen() {
        
      this.navigation.navigate("Details");
      
    }
    
  },
  mounted(){

      setTimeout(() => {

          this.goToHomeScreen()
      }, 5000);
  }
}
</script>

<style>
.container {
  background-color: #F4F4F4;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>