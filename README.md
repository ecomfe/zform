zform
=====

从lego.baidu.com中独立出来的一个表单生成和编辑的工具，方便用户对复杂格式的数据进行编辑操作。例如：

```javascript
var options = [
  {
    'name': 'title',
    'display_name': '标题',
    'datatype': 'string',
    'rules': {
      'required': true,
      'max_length': 100,
      'min_length': 20
    }
  },
  {
    'name': 'age',
    'display_name': '年龄',
    'datatype': 'number',
    'rules': {
      'required': true,
      'max': 100,
      'min': 20
    }
  }
];
var form = require( 'zform ').create( options );
```

用户输入数据之后，调用：`form.getValue()`即可获取JSON格式的数据：

```javascript
{
  "title": "Hello World",
  "age": 40
}
```
