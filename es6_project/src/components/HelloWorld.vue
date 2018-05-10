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
      /* // let,const声明的变量只在它所在的代码块有效
      {
        var a = 10;
        let b = 1;
        const c = 2;
      }
      console.log(a) // 10
      console.log(b)  //ReferenceError: b is not defined. */

      /* // let，const不能重复声明已存在的变量
      var a = "aaa";
      var a = "AAA"
      console.log(a) // AAA
      let b = "bbb";
      // let b = "BBB"
      console.log(b) //报错 */



    // let a = [];
    
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

  /* // 以前，为变量赋值，只能直接指定值
  let a = 1;
  let b = 2;
  let c = 3;
  // ES6允许写成下面这样
  let [a,b,c] = [1,2,3];
  console.log(b)
  let object = {d:4,e:5,f:6}
  let {d,e,f} = {d:4,e:5,f:6}
  console.log(object.d)
  console.log(e) */



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
  /* var scenario = 'One winter morning,'  
      + 'an employee explained why he '
      + 'had shown up for work 45 minutes late.' 
    
  let scenario2 = `One winter morning,
      an employee explained why he
      had shown up for work 45 minutes late.`

      this.txt1 = scenario
      this.txt2 = scenario2 */

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
  
  /* let wait1000 = ()=> new Promise((resolve, reject)=> {setTimeout(resolve, 1000)});
  // let wait1000 = function() {
  //   return new Promise(function(resolve,reject) {
  //     return setTimeout(resolve,1000)
  //   })
  // }  
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
      }) */





      





















    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
</style>
