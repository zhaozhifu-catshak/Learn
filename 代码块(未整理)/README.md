# 代码块（未整理）

- 以特殊字符'^^'拼接两个字符形成一个新的字符串

```
    var message=['111','2222','333','444','555'];
    var Mess = message.slice(message.length-2); //筛选message数组最后两个元素
    console.log('Mess数组的值:',Mess);
    var MESS = '';
    for (var i =0; i<Mess.length;i++){
      if(i==Mess.length-1){
        MESS += Mess[i] 
      }else{
        MESS += Mess[i] + '^^'
        }
    };

/**
  *第二个例子
  *
  **/
    var message=['111','2222','333','444','555'];
    var Mess = message.slice(message.length-2); //筛选message数组最后两个元素
    console.log('Mess数组的值:',Mess);
    var MESS = '';
    for (var i =0; i<Mess.length-1;i++){
       MESS += Mess[i] + '^^'
    };
    console.log( MESS + Mess[Mess.length-1] );

```



- 根据数组里对象selected值得属性判断,并把id的值拼接起来
```
const selectid = [
  {address:"哈尔滨" id:"1",led_size:"256X64", listPicture:"/image/myleds.jpg", name:"屏本事",num:"1",online:"在线",price:"0.01",
remark:"null",selected:true,usable_time:"9:00--16:00"}
  {address:"哈尔滨",id:"2",led_size:"64X32",listPicture:"/image/myleds.jpg",name:"屏本事2",num:"1",online:"在线",price:"0.01",remark:"null",selected:true,usable_time:"9:30--23:30"}
]

var ids = '';
    for (var i = 0; i < selectid.length; i++) {
      if (true == selectid[i].selected) {
        ids += selectid[i].id+",";
      }
    };
    if(ids!=""){
      ids=ids.substring(0,ids.length-1);
    }
console.log(ids); //1,2
```

DOM节点：
```
<!-- HTML结构 -->
<div id="test-div">
<div class="c-red">
    <p id="test-p">JavaScript</p>
    <p>Java</p>
  </div>
  <div class="c-red c-green">
    <p>Python</p>
    <p>Ruby</p>
    <p>Swift</p>
  </div>
  <div class="c-green">
    <p>Scheme</p>
    <p>Haskell</p>
  </div>
</div>
```
请选择出指定条件的节点：
```
'use strict';
// 选择<p>JavaScript</p>:
var js = document.getElementById('test-p');

// 选择<p>Python</p>,<p>Ruby</p>,<p>Swift</p>:
var arr = document.getElementById('test-div').getElementsByClassName("c-red c-green")[0].getElementsByTagName('p');

// 选择<p>Haskell</p>:
var haskell = document.getElementById('test-div').getElementsByClassName("c-green")[1].lastElementChild;

// 测试:
if (!js || js.innerText !== 'JavaScript') {
    alert('选择JavaScript失败!');
} else if (!arr || arr.length !== 3 || !arr[0] || !arr[1] || !arr[2] || arr[0].innerText !== 'Python' || arr[1].innerText !== 'Ruby' || arr[2].innerText !== 'Swift') {
    console.log('选择Python,Ruby,Swift失败!');
} else if (!haskell || haskell.innerText !== 'Haskell') {
    console.log('选择Haskell失败!');
} else {
    console.log('测试通过!');
}
```