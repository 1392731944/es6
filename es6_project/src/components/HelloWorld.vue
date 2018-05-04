<template>
  <div class="Index">
    <!-- <h1>{{ title }}</h1> -->
    <el-button @click="test()" type="success">测试按钮</el-button>
    <p>{{ txt1 }}</p>
    <p>{{ txt2 }}</p>
  </div>
</template>

<script>
export default {
  data () {
    return { 
      title: 'es6',
      txt1:'',
      txt2:''
    }
  },
  created(){
    // this.test();
  },
  methods:{
    test(){
      // let声明的变量只在它所在的代码块有效
      /* {
        let a = 10;
        var b = 1;
      }
      console.log(a) // ReferenceError: a is not defined.
      console.log(b)  //1 */

    let a = [];
    
   /*  for (var i = 0;i < 10; i++) {
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
   
  /* for (let i = 0; i < 10; i++) {
    a[i] = function () {
      let i = "abc"
      console.log(i);
    };
  }
  // a[i]打印出i
  a[6](); // 6
  console.log(i) //ReferenceError: i is not defined */


  //解构赋值
  // let [b,c,d] = [1,2,3];
  // console.log(b)
  // let {e,f,g} = {e:1,f:5,g:6}
  // console.log(e)

  //默认参数
  /* var link = function (height, color, url) {  
    var height = height || 50;  
    var color = color || 'red';  
    var url = url || 'http://4px.com';
    console.log(height)
    console.log(color)  
    console.log(url)
  }
  link(10)

  let linkTwo = (height = 20, color = "red", url = 'http://4px.com') => {
    console.log(height)
    console.log(color)
    console.log(url)
  }
  linkTwo(30) */

  // 模板对象
  /* var name = 'Your name is ' + first + ' ' + last + '.';  
  var url = 'http://localhost:3000/api/messages/' + id;


  var name = `Your name is ${first} ${last}.`;  
  var url = `http://localhost:3000/api/messages/${id}`; */


  // 多行字符串
  var scenario = 'One winter morning,'  
      + 'an employee explained why he '
      + 'had shown up for work 45 minutes late.' 
    
  let scenario2 = `One winter morning,
      an employee explained why he
      had shown up for work 45 minutes late.`

      this.txt1 = scenario
      this.txt2 = scenario2

  //箭头函数
  

  //Promises

 /*  setTimeout(function(){  
    console.log('Yay!');  
  }, 1000); */ 

  /* var wait1000 =  new Promise(function(resolve, reject) {  
    setTimeout(resolve, 1000);  
  }).then(function() {  
    console.log('Yay!');  
  }); */

  /* var wait1000 =  new Promise((resolve, reject)=> {  
    setTimeout(resolve, 1000);  
  }).then(()=> {  
    console.log('Yay!');  
  }); */

  // setTimeout(function(){  
  //   console.log('one');  
  //   setTimeout(function(){  
  //     console.log('two');
  //     setTimeout(function(){
  //       console.log('three');
  //       setTimeout(function () {
  //         console.log('four')
  //       },1000)
  //     },1000)  
  //   }, 1000)  
  // }, 1000);
  
  let wait1000 = ()=> new Promise((resolve, reject)=> {setTimeout(resolve, 1000)});  
  wait1000()  
      .then(()=> {  
        console.log('one')  
        return wait1000()  
      })  
      .then(()=> {  
        console.log('two')
        return wait1000()  
      })
      .then(()=> {
        console.log('three')
        return wait1000()
      })
      .then(()=> {
        console.log('four')
      })





      





















    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
</style>
