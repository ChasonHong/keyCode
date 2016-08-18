## 简介：
#### js获取键盘按键的键码: event.keyCode，记录-方便查找。
### 1、键盘各按键对应的数字
![](https://github.com/ChasonHong/keyCode/blob/master/keycode.png)

```javascript
//查看按键键码
document.onkeydown = function(event) {
    console.log(event.keyCode);
};
```
### 2、键盘码使用
###### 2.1、原生js使用

```javascript
document.onkeyup = function(event) {
    var e = event ? event : window.event;
    if (e.keyCode == 13) {//旧版火狐、Opera请使用e.which
        alert('您按了回车键。');
    }
};
```

###### 2.2、jQuery使用
```javascript
$(document).on('keyup',function(event) {
    if (event.keyCode == 13) {
        alert('您按了回车键。');
    }
});
```
### 3、结束语
###### 本文有任何错误，或有任何疑问，欢迎留言说明[Issues](https://github.com/ChasonHong/keyCode/issues/new)。
