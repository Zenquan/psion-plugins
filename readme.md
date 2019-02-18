## psion-plugins

### 背景

>首先，一些项目中如果只是单纯需要一个插件，不需要引入相对庞大的库。然后，为了锻炼自己的原生js能力与一些设计模式能力。基于以上两个原因，就有了这个仓库的想法。

### 文档
#### 联动器
效果：
- [两级联动和三级联动]()
安装
```js
<script src="./address.js"></script>
<script src="./address-plugin.js"></script>
```
- 两级联动
```js
new address({
  pro: document.querySelector('#pro1'),
  city: document.querySelector('#city1'),
});
```
- 三级联动
```js
new address({
  pro: document.querySelector('#pro'),
  city: document.querySelector('#city'),
  area: document.querySelector('#area'),
  defaultPro: '浙江省',
  defaultCity: '杭州市',
  defaultArea: '淳安县',
});
```
**中间发现了select元素中可通过dom获取selectedIndex属性**
```js
 <select name="" id="test">
    <option value="1">1</option>
    <option value="2">2</option>
    <option value="3">3</option>
  </select>
  <script>
    var test = document.querySelector('#test');
    test.onchange= function() {
      console.log(this.selectedIndex);
    }
  </script>
```