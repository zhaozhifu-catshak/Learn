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

