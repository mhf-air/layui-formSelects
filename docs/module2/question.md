# 常见问题

> 1.什么是formSelects

formSelects是基于Layui诞生的多选解决方案, 在Layui原有的select基础上实现了多选


> 2.哪里下载formSelects

[https://github.com/hnzzmsf/layui-formSelects](https://github.com/hnzzmsf/layui-formSelects)


> 3.有问题怎么办

在 [学习交流](/module/study) 中, 可以联系作者, 或者加群和小伙伴交流


> 4.formSelects的作者是谁

`maplemei`, 一个热爱前端的Java程序猿, QQ: 707200833


> 5.如何使用formSelects

[快速开始](/README?id=%e5%bf%ab%e9%80%9f%e4%b8%8a%e6%89%8b)


> 6.xm-select是什么

`xm-select`是一个自定义属性, 在`select`标签上标记后, 此标签将会被转化为多选, 其中`xm-select`对应的值将变为这个多选的ID, 切记请保证此值唯一


> 7.如何反馈问题

加作者QQ, 或者加群, 截图、贴代码、发问题原因


> 8.如何获取已选择的值

```js
formSelects.value('xm-id');
```


> 9.如何获取设置值

```js
formSelects.value('xm-id', ['1', '2', '3']);
```


> 10.如何查看版本

打开源码, 最上面显示的version


> 11.为什么远程搜索发送的是`json`数据

```
//formSelects.config方式是有三个参数的, 示例上第三个参数为true

**
 * 1.配置远程搜索, 请求头, 请求参数, 请求类型等
 *
 * formSelects.config(ID, Options, isJson);
 *
 * @param ID        xm-select的值
 * @param Options   配置项
 * @param isJson    是否传输json数据, true将添加请求头 Content-Type: application/json; charset=UTF-8
 */

```