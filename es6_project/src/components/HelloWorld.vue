<template>
  <div class="Index">
    <h1>{{ title }}</h1>
    <el-button @click="test()" type="success">测试按钮</el-button>
  </div>
</template>

<script>
export default {
  data () {
    return { 
      title: 'es6',
    }
  },
  created(){
    // this.test();
  },
  methods:{
    test(){
      /* {
        let a = 10;
        var b = 1;
      }
      console.log(a) // ReferenceError: a is not defined.
      console.log(b)  //1 */

    var a = [];

    /* for (var i = 0;i < 10; i++) {
      a[i] = function () {
        console.log(i);
      };
    }
    a[6](); // 10
    console.log(i) //10 */

   /* var i = 0;
   for (i; i < 10; i++) {
      a[i] = function () {
        console.log(i);
      };
    }
    a[6](); // 10
    console.log(i) //10 */
   
  for (let i = 0; i < 10; i++) {
    a[i] = function () {
      let i = "abc"
      console.log(i);
    };
  }
  // a[i] === i
  a[6](); // 6




    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
</style>
