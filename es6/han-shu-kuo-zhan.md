##函数新增特性

- 参数默认值

- rest参数

- 扩展运算符

- 箭头函书

- this绑定

- 尾调用



##参数默认值,后边不能有不带默认值的参数

```
{
    function test(x, y = 'world'){
        console.log('默认值', x, y);
    }
    test('hello');
    test('hello', 'kill');
}
```



```
{
    let x = 'test';
    function test2(x, y = x){
        console.log('作用域', x, y);
    }
    test2('kill');    //作用域 kill kill
    test2();    //作用域 undefined undefined
}
```


##rest参数,后边不能再有其他参数

```
{
    function test3(..arg){
        for(let v if arg){
            console.log('rest', v);
        }
    }
    test3(1, 2, 3, 4, 'a');
}
```


##扩展运算符

{
    console.log('a', ...[1, 2, 4]);    //a 1 2 4
}




##箭头函数

![](/assets/360截图20171113222156916.jpg)



##尾调用

- 提升性能

```
{
    function tail(){
        console.log('tail', x);
    }
    
    function fx(){
        return tail(x)
    }
    
    fx(123)；    //tail 123
}
```










