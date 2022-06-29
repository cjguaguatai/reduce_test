<template>
  <div>
    <div>
      <span>选择所在地区：</span>
      <input type="radio"  name="area" v-model="area" :value="1">中国大陆
      <input type="radio"  name="area" v-model="area" :value="2">中国香港
    </div>
    <div>
      <span>手机号码：</span>
      <input type="text" name="phone" v-model.number="phone">
    </div>
    <div>
      <span>年龄: </span>
      <input type="text" name="age" v-model.number="age">
    </div>
    <div>
      <span>密码：</span>
      <input type="password" name="password" v-model="password">
    </div>
    <div>
      <span>爱好：</span>
      <input type="checkbox" v-model="checkbox" value="看书">看书
      <input type="checkbox" v-model="checkbox" value="学习">学习
      <input type="checkbox" v-model="checkbox" value="写代码">写代码
      <input type="checkbox" v-model="checkbox" value="游戏">游戏
    </div>
    <div>
      <input type="checkbox" v-model="jizhu"> 记住密码
    </div>
    ================================================================
    <div>
      我来自：{{{'1':'中国大陆','2':'中国香港'}[area]}}
      <br>
      手机号码是：{{password}}
      <br>
      年龄是：{{age}}
      <br>
      密码是：{{password}}
      <br>
      爱好是：{{checkbox.join('-')}}
      <br>
      是否记住密码：{{jizhu}}
    </div>


  </div>
</template>

<script>
export default {
  data() {
    return {  
      area:1,
      phone:'',
      age:'',
      password:'',
      checkbox:[],
      jizhu:true
    };
  }
}
</script>