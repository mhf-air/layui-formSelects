
> vue写法


```html
<select name="city" v-xm-select="xmSelect1">
	<option value="1" disabled="disabled">北京</option>
    <option value="2" selected="selected">上海</option>
    <option value="3">广州</option>
    <option value="4" selected="selected">深圳</option>
    <option value="5">天津</option>
</select>

<select name="city" v-xm-select="xmSelect2">
	<option v-for="item in arr" :value="item.value" :disabled="!!item.disabled" v-text="item.name"></option>
</select>
```

```js
new Vue({
	el: '#app',
	data: {
		xmSelect1: {
			id: 'vue-example1',
			vals: ['1', '2'],
		},
		xmSelect2: {
			id: 'vue-example2',
			vals: ['1'],
		},
		arr: [
			{"name":"北京","value":1,"selected":"","disabled":""},
		    {"name":"上海","value":2,"selected":"","disabled":""},
		    {"name":"广州","value":3,"selected":"selected","disabled":""},
		    {"name":"深圳","value":4,"selected":"","disabled":"disabled"},
		    {"name":"天津","value":5,"selected":"","disabled":""}
		],
	}
});
```

> 示例

<div id="vue-example">
	<select name="city" v-xm-select="xmSelect1">
		<option value="1" disabled="disabled">北京</option>
	    <option value="2" selected="selected">上海</option>
	    <option value="3">广州</option>
	    <option value="4" selected="selected">深圳</option>
	    <option value="5">天津</option>
	</select>
	
	<hr/>
	
	<select name="city" v-xm-select="xmSelect2">
		<option v-for="item in arr" :value="item.value" :disabled="!!item.disabled" v-text="item.name"></option>
	</select>
</div>

`F12`打开控制台可以尝试修改下vue data值

```js
//修改`vals` == 修改选中数据
//新增选中项 广州
vueApp.$data.xmSelect1.vals.push('3');

//追加选项 台湾
vueApp.$data.arr.push({"name":"台湾","value":6});
```

这只是一个简单的开始~~~


<script>
window.vueApp = new Vue({
	el: '#vue-example',
	data: {
		xmSelect1: {
			id: 'vue-example1',
			vals: ['1', '2'],
		},
		xmSelect2: {
			id: 'vue-example2',
			vals: ['1'],
		},
		arr: [
			{"name":"北京","value":1},
		    {"name":"上海","value":2},
		    {"name":"广州","value":3},
		    {"name":"深圳","value":4,"disabled":"disabled"},
		    {"name":"天津","value":5}
		],
	}
});
</script>

