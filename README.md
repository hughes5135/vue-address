# vue-address
> 基于vue.js的多级联动地址选择器，需要配合element-ui使用
* [源码](https://github.com/peng1992/vue-address/blob/master/src/components/address.vue)
* [在线DOM](https://webcodefarmer.github.io/vue-address/)

#### 如何使用？

在`vue-cli` + `element-ui` 的项目中，把`address.vue`单文件copy到你的项目目录里就可以啦！

```
<template>
  <div id="app">
    <img src="./assets/logo.png">
    <vue-address
      :province="province"
      :city="city"
      :detail="detail"
      :district="district"
      @change="handlerChange"
    ></vue-address>
  </div>
</template>

<script>
import vueAddress from './components/address'
export default {
  components: {
    vueAddress
  },
  data: function() {
    return {
      province:'',
      city:'',
      district:'',
      detail:''
    }
  },
  methods: {
    handlerChange: function (val) {
      console.log(val);
    }
  }
}
</script>
<style>
#app {text-align: center;color: #2c3e50;margin-top: 60px;}
</style>
```

#### vue-address属性
* province	省
* city      市
* district  区/县
* detail    详细地址

#### vue-address事件
* change  当省、市、区/县、详细地址任一值改变时触发
