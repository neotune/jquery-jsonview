# jQuery JSONView

JSON 데이터를 깔끔하게 볼 수 있게 하는 jquery plugin 입니다.
해당 소스의 원본은 아래의 사이트에서 TEST 및 다운로드 받으 실 수 있습니다.

Port of Ben Hollis's JSONView extension for Firefox: http://jsonview.com

[Live demo](http://blog.yesmeck.com/jquery-jsonview/)

## example

#### HTML

```xml
<link rel="stylesheet" href="jquery.jsonview.css" />
<script type="text/javascript" src="jquery.min.js"></script>
<script type="text/javascript" src="jquery.jsonview.js"></script>
```
#### javascript
```javascript
var json = {"hey": "guy","anumber": 243,"anobject": {"whoa": "nuts","anarray": [1,2,"thr<h1>ee"], "more":"stuff"},"awesome": true,"bogus": false,"meaning": null, "japanese":"明日がある。", "link": "http://jsonview.com", "notLink": "http://jsonview.com is great"};

$(function() {
  $("#json").JSONView(json);
  // with options
  $("#json-collasped").JSONView(json, { collapsed: true });
});
```

### Options

jQuery JSONView can be configured using the following options.

* `collapsed` - Collapse all nodes when rendering first time, default is `false`.
* `nl2br` - Convert new line to `<br>` in String, default is `false`.
* `recursive_collapser` - Collapse nodes recursively, default is `false`.
* `escape` - Escape HTML in key, default is `true`.

### API

jQuery JSONView provide following methods to allow you control JSON nodes, all methods below accept a level argument to perform action on the specify node.

* `jQuery#JSONView('collapse', [level])` - Collapse nodes.
* `jQuery#JSONView('expand', [level])` - Expand nodes.
* `jQuery#JSONView('toggle', [level])` -  Toggle nodes.

## Licence

[MIT](http://opensource.org/licenses/MIT)
