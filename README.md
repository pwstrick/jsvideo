# JavaScript录屏和回放

插件没有任何参数，下面是初始化代码，在内部就已经打开监控，开始录制。

```javascript
const video = new JSVideo();
```

下面是一个简单的示例，修改两个文本框中的属性或值。

```javascript
const input = document.querySelector("[name=name]"),
    mobile = document.querySelector("[name=mobile]");
//修改placeholder属性
setTimeout(function() {
    input.setAttribute("placeholder", "name");
}, 1000);
//setTimeout(function() {
//    input.setAttribute("autocomplete", "on");
//}, 2000);
//修改姓名的value值
setTimeout(function() {
    input.value = "Strick";
}, 3000);
//修改手机的value值
setTimeout(function() {
    mobile.value = "13800138000";
}, 4000);
//在iframe中回放
setTimeout(function() {
    video.createIframe();
}, 5000);
```

关于插件的原理，可参考《[纯JavaScript实现页面行为的录制](https://www.cnblogs.com/strick/p/12206766.html)》一文。