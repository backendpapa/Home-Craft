<template>
 <!-- <view> -->
      <!-- <View> -->
        <app-navigator ></app-navigator>
      <!-- </View> -->
 <!-- </view> -->
</template>
<script>
import {
  createAppContainer,
  createStackNavigator,
} from "vue-native-router";

import {BackHandler, Alert,View } from 'react-native'
import HomeScreen from "./screens/HomeScreen.vue";
import DetailsScreen from "./screens/DetailsScreen.vue";
import LoginScreen from './screens/LoginScreen.vue'
const StackNavigator = createStackNavigator(
  {
   
    Home: {
      screen:HomeScreen,
      navigationOptions: {
        header: null,
        
      }
    },
    Details: {
      screen:DetailsScreen,
      navigationOptions: {
        header: null,
      }
    },
    Login: {
      screen:LoginScreen,
      navigationOptions: {
        header: null,
      }
    },
  },
  {
    initialRouteName: 'Home',
  },
  {
  headerMode: 'none',
}
);

const AppNavigator = createAppContainer(StackNavigator);

export default {
  components: { AppNavigator },
  data(){
    return {
      splash:5000
    }
  },
  methods:{
    onBackPress(){
      Alert.alert('hello')
    }
  },
  mounted(){
    // BackHandler.addEventListener('hardwareBackPress', this.onBackPress());
    
  }
}
</script>
<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
