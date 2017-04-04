# api documentation for  [squel (v5.8.0)](https://github.com/hiddentao/squel#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-squel.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-squel) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-squel.svg)](https://travis-ci.org/npmdoc/node-npmdoc-squel)
#### SQL query string builder

[![NPM](https://nodei.co/npm/squel.png?downloads=true)](https://www.npmjs.com/package/squel)

[![apidoc](https://npmdoc.github.io/node-npmdoc-squel/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-squel_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-squel/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-squel/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-squel/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ramesh Nair",
        "email": "ram@hiddentao.com",
        "url": "http://www.hiddentao.com/"
    },
    "bugs": {
        "url": "https://github.com/hiddentao/squel/issues"
    },
    "contributors": [
        {
            "name": "Ramesh Nair",
            "email": "ram@hiddentao.com",
            "url": "http://www.hiddentao.com/"
        },
        {
            "name": "Sergej Brjuchanov",
            "email": "serges@seznam.cz"
        }
    ],
    "dependencies": {},
    "description": "SQL query string builder",
    "devDependencies": {
        "babel-preset-es2015": "^6.6.0",
        "chai": "1.5.x",
        "coffee-script": "^1.10.0",
        "gulp": "^3.9.1",
        "gulp-babel": "^6.1.2",
        "gulp-concat": "^2.6.0",
        "gulp-insert": "^0.5.0",
        "gulp-istanbul": "^1.1.1",
        "gulp-mocha": "^2.2.0",
        "gulp-replace": "^0.5.4",
        "gulp-uglify": "^1.5.3",
        "gulp-umd": "^0.2.0",
        "load-grunt-tasks": "~0.1.0",
        "mocha": "1.9.x",
        "run-sequence": "^1.1.5",
        "sinon": "1.6.x",
        "time-grunt": "~0.1.1",
        "uglify-js": "1.3.x",
        "underscore": "1.4.x",
        "yargs": "^4.7.1"
    },
    "directories": {},
    "dist": {
        "shasum": "49d144ef95d0b057da90544b4e1200b08965795f",
        "tarball": "https://registry.npmjs.org/squel/-/squel-5.8.0.tgz"
    },
    "engines": {
        "node": ">= 0.12.0"
    },
    "gitHead": "771e9ab075bad1c7932aeacff0ea93e600f27df4",
    "homepage": "https://github.com/hiddentao/squel#readme",
    "keywords": [
        "sql",
        "database",
        "rdbms"
    ],
    "main": "dist/squel.js",
    "maintainers": [
        {
            "name": "hiddentao",
            "email": "ram@hiddentao.com"
        }
    ],
    "name": "squel",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/hiddentao/squel.git"
    },
    "scripts": {
        "build": "gulp",
        "prepublish": "npm run build",
        "test": "gulp"
    },
    "version": "5.8.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module squel](#apidoc.module.squel)
1.  [function <span class="apidocSignatureSpan">squel.</span>case (name, options)](#apidoc.element.squel.case)
1.  [function <span class="apidocSignatureSpan">squel.</span>delete (options, blocks)](#apidoc.element.squel.delete)
1.  [function <span class="apidocSignatureSpan">squel.</span>expr (options)](#apidoc.element.squel.expr)
1.  [function <span class="apidocSignatureSpan">squel.</span>insert (options, blocks)](#apidoc.element.squel.insert)
1.  [function <span class="apidocSignatureSpan">squel.</span>registerValueHandler (type, handler)](#apidoc.element.squel.registerValueHandler)
1.  [function <span class="apidocSignatureSpan">squel.</span>remove (options, blocks)](#apidoc.element.squel.remove)
1.  [function <span class="apidocSignatureSpan">squel.</span>rstr ()](#apidoc.element.squel.rstr)
1.  [function <span class="apidocSignatureSpan">squel.</span>select (options, blocks)](#apidoc.element.squel.select)
1.  [function <span class="apidocSignatureSpan">squel.</span>str ()](#apidoc.element.squel.str)
1.  [function <span class="apidocSignatureSpan">squel.</span>update (options, blocks)](#apidoc.element.squel.update)
1.  [function <span class="apidocSignatureSpan">squel.</span>useFlavour ()](#apidoc.element.squel.useFlavour)
1.  object <span class="apidocSignatureSpan">squel.</span>cls
1.  object <span class="apidocSignatureSpan">squel.</span>flavour
1.  object <span class="apidocSignatureSpan">squel.</span>flavours
1.  string <span class="apidocSignatureSpan">squel.</span>VERSION

#### [module squel.cls](#apidoc.module.squel.cls)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>AbstractConditionBlock (options)](#apidoc.element.squel.cls.AbstractConditionBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>AbstractSetFieldBlock (options)](#apidoc.element.squel.cls.AbstractSetFieldBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>AbstractTableBlock (options, prefix)](#apidoc.element.squel.cls.AbstractTableBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>AbstractVerbSingleValueBlock (options)](#apidoc.element.squel.cls.AbstractVerbSingleValueBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>BaseBuilder (options)](#apidoc.element.squel.cls.BaseBuilder)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Block (options)](#apidoc.element.squel.cls.Block)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Case (fieldName)](#apidoc.element.squel.cls.Case)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Cloneable ()](#apidoc.element.squel.cls.Cloneable)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Delete (options)](#apidoc.element.squel.cls.Delete)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>DistinctBlock ()](#apidoc.element.squel.cls.DistinctBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Expression (options)](#apidoc.element.squel.cls.Expression)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>FromTableBlock (options)](#apidoc.element.squel.cls.FromTableBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>FunctionBlock (options)](#apidoc.element.squel.cls.FunctionBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>GetFieldBlock (options)](#apidoc.element.squel.cls.GetFieldBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>GroupByBlock (options)](#apidoc.element.squel.cls.GroupByBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>HavingBlock (options)](#apidoc.element.squel.cls.HavingBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Insert (options)](#apidoc.element.squel.cls.Insert)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>InsertFieldValueBlock ()](#apidoc.element.squel.cls.InsertFieldValueBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>InsertFieldsFromQueryBlock (options)](#apidoc.element.squel.cls.InsertFieldsFromQueryBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>IntoTableBlock (options)](#apidoc.element.squel.cls.IntoTableBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>JoinBlock (options)](#apidoc.element.squel.cls.JoinBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>LimitBlock (options)](#apidoc.element.squel.cls.LimitBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>OffsetBlock (options)](#apidoc.element.squel.cls.OffsetBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>OrderByBlock (options)](#apidoc.element.squel.cls.OrderByBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>QueryBuilder (options, blocks)](#apidoc.element.squel.cls.QueryBuilder)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Select (options)](#apidoc.element.squel.cls.Select)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>SetFieldBlock ()](#apidoc.element.squel.cls.SetFieldBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>StringBlock (options, str)](#apidoc.element.squel.cls.StringBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>TargetTableBlock ()](#apidoc.element.squel.cls.TargetTableBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>UnionBlock (options)](#apidoc.element.squel.cls.UnionBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>Update (options)](#apidoc.element.squel.cls.Update)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>UpdateTableBlock ()](#apidoc.element.squel.cls.UpdateTableBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>WhereBlock (options)](#apidoc.element.squel.cls.WhereBlock)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>isSquelBuilder (obj)](#apidoc.element.squel.cls.isSquelBuilder)
1.  [function <span class="apidocSignatureSpan">squel.cls.</span>registerValueHandler (type, handler)](#apidoc.element.squel.cls.registerValueHandler)
1.  object <span class="apidocSignatureSpan">squel.cls.</span>DefaultQueryBuilderOptions
1.  object <span class="apidocSignatureSpan">squel.cls.</span>globalValueHandlers

#### [module squel.flavours](#apidoc.module.squel.flavours)
1.  [function <span class="apidocSignatureSpan">squel.flavours.</span>mssql (_squel)](#apidoc.element.squel.flavours.mssql)
1.  [function <span class="apidocSignatureSpan">squel.flavours.</span>mysql (_squel)](#apidoc.element.squel.flavours.mysql)
1.  [function <span class="apidocSignatureSpan">squel.flavours.</span>postgres (_squel)](#apidoc.element.squel.flavours.postgres)



# <a name="apidoc.module.squel"></a>[module squel](#apidoc.module.squel)

#### <a name="apidoc.element.squel.case"></a>[function <span class="apidocSignatureSpan">squel.</span>case (name, options)](#apidoc.element.squel.case)
- description and source-code
```javascript
function _case(name, options) {
  return new cls.Case(name, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.delete"></a>[function <span class="apidocSignatureSpan">squel.</span>delete (options, blocks)](#apidoc.element.squel.delete)
- description and source-code
```javascript
function _delete(options, blocks) {
  return new cls.Delete(options, blocks);
}
```
- example usage
```shell
...
.toString()
'''

### DELETE

'''javascript
// DELETE FROM test
squel.delete()
.from("test")
.toString()

// DELETE FROM table1 WHERE (table1.id = 2) ORDER BY id DESC LIMIT 2
squel.delete()
.from("table1")
.where("table1.id = ?", 2)
...
```

#### <a name="apidoc.element.squel.expr"></a>[function <span class="apidocSignatureSpan">squel.</span>expr (options)](#apidoc.element.squel.expr)
- description and source-code
```javascript
function expr(options) {
  return new cls.Expression(options);
}
```
- example usage
```shell
...

### Expression builder

There is also an expression builder which allows you to build complex expressions for 'WHERE' and 'ON' clauses:

'''javascript
// test = 3 OR test = 4
squel.expr()
.or("test = 3")
.or("test = 4")
.toString()

// test = 3 AND (inner = 1 OR inner = 2) OR (inner = 3 AND inner = 4 OR (inner IN ('str1, 'str2', NULL)))
squel.expr()
.and("test = 3")
...
```

#### <a name="apidoc.element.squel.insert"></a>[function <span class="apidocSignatureSpan">squel.</span>insert (options, blocks)](#apidoc.element.squel.insert)
- description and source-code
```javascript
function insert(options, blocks) {
  return new cls.Insert(options, blocks);
}
```
- example usage
```shell
...
.toString()
'''

### INSERT

'''javascript
// INSERT INTO test (f1) VALUES (1)
squel.insert()
.into("test")
.set("f1", 1)
.toString()

// INSERT INTO test (name, age) VALUES ('Thomas', 29), ('Jane', 31)
squel.insert()
.into("test")
...
```

#### <a name="apidoc.element.squel.registerValueHandler"></a>[function <span class="apidocSignatureSpan">squel.</span>registerValueHandler (type, handler)](#apidoc.element.squel.registerValueHandler)
- description and source-code
```javascript
registerValueHandler = function (type, handler) {
  _registerValueHandler(cls.globalValueHandlers, type, handler);
}
```
- example usage
```shell
...
### Custom value types

By default Squel does not support the use of object instances as field values. Instead it lets you tell it how you want
specific object types to be handled:

'''javascript
// handler for objects of type Date
squel.registerValueHandler(Date, function(date) {
return date.getFullYear() + '/' + (date.getMonth() + 1) + '/' + date.getDate();
});

squel.update().
.table('students')
.set('start_date', new Date(2013, 5, 1))
.toString()
...
```

#### <a name="apidoc.element.squel.remove"></a>[function <span class="apidocSignatureSpan">squel.</span>remove (options, blocks)](#apidoc.element.squel.remove)
- description and source-code
```javascript
function _delete(options, blocks) {
  return new cls.Delete(options, blocks);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.rstr"></a>[function <span class="apidocSignatureSpan">squel.</span>rstr ()](#apidoc.element.squel.rstr)
- description and source-code
```javascript
function rstr() {
  var inst = new cls.FunctionBlock({
    rawNesting: true
  });
  inst.function.apply(inst, arguments);
  return inst;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.select"></a>[function <span class="apidocSignatureSpan">squel.</span>select (options, blocks)](#apidoc.element.squel.select)
- description and source-code
```javascript
function select(options, blocks) {
  return new cls.Select(options, blocks);
}
```
- example usage
```shell
...

var squel = require("squel");

### SELECT

'''javascript
// SELECT * FROM table
squel.select()
.from("table")
.toString()

// SELECT t1.id, t2.name FROM table 't1' LEFT JOIN table2 't2' ON (t1.id = t2.id) WHERE (t2.name <> 'Mark') AND (t2.name <> 'John
') GROUP BY t1.id
squel.select()
.from("table", "t1")
.field("t1.id")
...
```

#### <a name="apidoc.element.squel.str"></a>[function <span class="apidocSignatureSpan">squel.</span>str ()](#apidoc.element.squel.str)
- description and source-code
```javascript
function str() {
  var inst = new cls.FunctionBlock();
  inst.function.apply(inst, arguments);
  return inst;
}
```
- example usage
```shell
...

// SELECT 't1'.'id', 't1'.'name' as "My name", 't1'.'started' as "Date" FROM table 't1' WHERE age IN (RANGE(1, 1.2)) ORDER BY id
 ASC LIMIT 20
squel.select({ autoQuoteFieldNames: true })
    .from("table", "t1")
    .field("t1.id")
    .field("t1.name", "My name")
    .field("t1.started", "Date")
    .where("age IN ?", squel.str('RANGE(?, ?)', 1, 1.2))
    .order("id")
    .limit(20)
    .toString()
'''

You can build parameterized queries:
...
```

#### <a name="apidoc.element.squel.update"></a>[function <span class="apidocSignatureSpan">squel.</span>update (options, blocks)](#apidoc.element.squel.update)
- description and source-code
```javascript
function update(options, blocks) {
  return new cls.Update(options, blocks);
}
```
- example usage
```shell
...
.toString()
'''

### UPDATE

'''javascript
// UPDATE test SET f1 = 1
squel.update()
.table("test")
.set("f1", 1)
.toString()

// UPDATE test, test2, test3 AS 'a' SET test.id = 1, test2.val = 1.2, a.name = "Ram", a.email = NULL, a.count = a.count + 1
squel.update()
.table("test")
...
```

#### <a name="apidoc.element.squel.useFlavour"></a>[function <span class="apidocSignatureSpan">squel.</span>useFlavour ()](#apidoc.element.squel.useFlavour)
- description and source-code
```javascript
useFlavour = function () {
  var flavour = arguments.length <= 0 || arguments[0] === undefined ? null : arguments[0];

  if (!flavour) {
    return squel;
  }

  if (squel.flavours[flavour] instanceof Function) {
    var s = _buildSquel(flavour);

    squel.flavours[flavour].call(null, s);

    // add in flavour methods
    s.flavours = squel.flavours;
    s.useFlavour = squel.useFlavour;

    return s;
  } else {
    throw new Error('Flavour not available: ' + flavour);
  }
}
```
- example usage
```shell
...

At the moment Squel provides 'mysql', 'mssql' and 'postgres' flavours which augment query builders with additional commands (e.g
. 'INSERT ... RETURNING'
for use with Postgres).

To use this in node.js:

'''javascript
var squel = require('squel').useFlavour('postgres');
'''

For the browser:

'''html
<script type="text/javascript" src="https://rawgithub.com/hiddentao/squel/master/squel.min.js"></script>
<script type="text/javascript">
...
```



# <a name="apidoc.module.squel.cls"></a>[module squel.cls](#apidoc.module.squel.cls)

#### <a name="apidoc.element.squel.cls.AbstractConditionBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>AbstractConditionBlock (options)](#apidoc.element.squel.cls.AbstractConditionBlock)
- description and source-code
```javascript
function _class23(options) {
  _classCallCheck(this, _class23);

  var _this27 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class23).call(this, options));

  _this27._conditions = [];
  return _this27;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.AbstractSetFieldBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>AbstractSetFieldBlock (options)](#apidoc.element.squel.cls.AbstractSetFieldBlock)
- description and source-code
```javascript
function _class14(options) {
  _classCallCheck(this, _class14);

  var _this16 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class14).call(this, options));

  _this16._reset();
  return _this16;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.AbstractTableBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>AbstractTableBlock (options, prefix)](#apidoc.element.squel.cls.AbstractTableBlock)
- description and source-code
```javascript
function _class8(options, prefix) {
  _classCallCheck(this, _class8);

  var _this10 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class8).call(this, options));

  _this10._tables = [];
  return _this10;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.AbstractVerbSingleValueBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>AbstractVerbSingleValueBlock (options)](#apidoc.element.squel.cls.AbstractVerbSingleValueBlock)
- description and source-code
```javascript
function _class20(options) {
  _classCallCheck(this, _class20);

  var _this24 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class20).call(this, options));

  _this24._value = 0;
  return _this24;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.BaseBuilder"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>BaseBuilder (options)](#apidoc.element.squel.cls.BaseBuilder)
- description and source-code
```javascript
function _class2(options) {
  _classCallCheck(this, _class2);

  var _this = _possibleConstructorReturn(this, Object.getPrototypeOf(_class2).call(this));

  var defaults = JSON.parse(JSON.stringify(cls.DefaultQueryBuilderOptions));

  _this.options = _extend({}, defaults, options);
  return _this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Block"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Block (options)](#apidoc.element.squel.cls.Block)
- description and source-code
```javascript
function _class5(options) {
  _classCallCheck(this, _class5);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class5).call(this, options));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Case"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Case (fieldName)](#apidoc.element.squel.cls.Case)
- description and source-code
```javascript
function _class4(fieldName) {
  var options = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];

  _classCallCheck(this, _class4);

  var _this6 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class4).call(this, options));

  if (_isPlainObject(fieldName)) {
    options = fieldName;

    fieldName = null;
  }

  if (fieldName) {
    _this6._fieldName = _this6._sanitizeField(fieldName);
  }

  _this6.options = _extend({}, cls.DefaultQueryBuilderOptions, options);

  _this6._cases = [];
  _this6._elseValue = null;
  return _this6;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Cloneable"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Cloneable ()](#apidoc.element.squel.cls.Cloneable)
- description and source-code
```javascript
function _class() {
  _classCallCheck(this, _class);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Delete"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Delete (options)](#apidoc.element.squel.cls.Delete)
- description and source-code
```javascript
function _class32(options) {
  var blocks = arguments.length <= 1 || arguments[1] === undefined ? null : arguments[1];

  _classCallCheck(this, _class32);

  blocks = blocks || [new cls.StringBlock(options, 'DELETE'), new cls.TargetTableBlock(options), new cls.FromTableBlock(_extend({},
options, {
    singleTable: true
  })), new cls.JoinBlock(options), new cls.WhereBlock(options), new cls.OrderByBlock(options), new cls.LimitBlock(options)];

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class32).call(this, options, blocks));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.DistinctBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>DistinctBlock ()](#apidoc.element.squel.cls.DistinctBlock)
- description and source-code
```javascript
function _class18() {
  _classCallCheck(this, _class18);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class18).apply(this, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Expression"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Expression (options)](#apidoc.element.squel.cls.Expression)
- description and source-code
```javascript
function _class3(options) {
  _classCallCheck(this, _class3);

  var _this5 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class3).call(this, options));

  _this5._nodes = [];
  return _this5;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.FromTableBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>FromTableBlock (options)](#apidoc.element.squel.cls.FromTableBlock)
- description and source-code
```javascript
function _class11(options) {
  _classCallCheck(this, _class11);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class11).call(this, _extend({}, options, {
    prefix: 'FROM'
  })));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.FunctionBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>FunctionBlock (options)](#apidoc.element.squel.cls.FunctionBlock)
- description and source-code
```javascript
function _class7(options) {
  _classCallCheck(this, _class7);

  var _this9 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class7).call(this, options));

  _this9._strings = [];
  _this9._values = [];
  return _this9;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.GetFieldBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>GetFieldBlock (options)](#apidoc.element.squel.cls.GetFieldBlock)
- description and source-code
```javascript
function _class13(options) {
  _classCallCheck(this, _class13);

  var _this15 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class13).call(this, options));

  _this15._fields = [];
  return _this15;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.GroupByBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>GroupByBlock (options)](#apidoc.element.squel.cls.GroupByBlock)
- description and source-code
```javascript
function _class19(options) {
  _classCallCheck(this, _class19);

  var _this23 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class19).call(this, options));

  _this23._groups = [];
  return _this23;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.HavingBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>HavingBlock (options)](#apidoc.element.squel.cls.HavingBlock)
- description and source-code
```javascript
function _class25(options) {
  _classCallCheck(this, _class25);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class25).call(this, _extend({}, options, {
    verb: 'HAVING'
  })));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Insert"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Insert (options)](#apidoc.element.squel.cls.Insert)
- description and source-code
```javascript
function _class33(options) {
  var blocks = arguments.length <= 1 || arguments[1] === undefined ? null : arguments[1];

  _classCallCheck(this, _class33);

  blocks = blocks || [new cls.StringBlock(options, 'INSERT'), new cls.IntoTableBlock(options), new cls.InsertFieldValueBlock(options
), new cls.InsertFieldsFromQueryBlock(options)];

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class33).call(this, options, blocks));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.InsertFieldValueBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>InsertFieldValueBlock ()](#apidoc.element.squel.cls.InsertFieldValueBlock)
- description and source-code
```javascript
function _class16() {
  _classCallCheck(this, _class16);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class16).apply(this, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.InsertFieldsFromQueryBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>InsertFieldsFromQueryBlock (options)](#apidoc.element.squel.cls.InsertFieldsFromQueryBlock)
- description and source-code
```javascript
function _class17(options) {
  _classCallCheck(this, _class17);

  var _this20 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class17).call(this, options));

  _this20._fields = [];
  _this20._query = null;
  return _this20;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.IntoTableBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>IntoTableBlock (options)](#apidoc.element.squel.cls.IntoTableBlock)
- description and source-code
```javascript
function _class12(options) {
  _classCallCheck(this, _class12);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class12).call(this, _extend({}, options, {
    prefix: 'INTO',
    singleTable: true
  })));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.JoinBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>JoinBlock (options)](#apidoc.element.squel.cls.JoinBlock)
- description and source-code
```javascript
function _class27(options) {
  _classCallCheck(this, _class27);

  var _this31 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class27).call(this, options));

  _this31._joins = [];
  return _this31;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.LimitBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>LimitBlock (options)](#apidoc.element.squel.cls.LimitBlock)
- description and source-code
```javascript
function _class22(options) {
  _classCallCheck(this, _class22);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class22).call(this, _extend({}, options, {
    verb: 'LIMIT'
  })));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.OffsetBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>OffsetBlock (options)](#apidoc.element.squel.cls.OffsetBlock)
- description and source-code
```javascript
function _class21(options) {
  _classCallCheck(this, _class21);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class21).call(this, _extend({}, options, {
    verb: 'OFFSET'
  })));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.OrderByBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>OrderByBlock (options)](#apidoc.element.squel.cls.OrderByBlock)
- description and source-code
```javascript
function _class26(options) {
  _classCallCheck(this, _class26);

  var _this30 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class26).call(this, options));

  _this30._orders = [];
  return _this30;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.QueryBuilder"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>QueryBuilder (options, blocks)](#apidoc.element.squel.cls.QueryBuilder)
- description and source-code
```javascript
function _class29(options, blocks) {
  _classCallCheck(this, _class29);

  var _this33 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class29).call(this, options));

  _this33.blocks = blocks || [];

  // Copy exposed methods into myself
  var _iteratorNormalCompletion14 = true;
  var _didIteratorError14 = false;
  var _iteratorError14 = undefined;

  try {
    for (var _iterator14 = _this33.blocks[Symbol.iterator](), _step14; !(_iteratorNormalCompletion14 = (_step14 = _iterator14.next
()).done); _iteratorNormalCompletion14 = true) {
      var block = _step14.value;

      var exposedMethods = block.exposedMethods();

      for (var methodName in exposedMethods) {
        var methodBody = exposedMethods[methodName];

        if (undefined !== _this33[methodName]) {
          throw new Error('Builder already has a builder method called: ' + methodName);
        }

        (function (block, name, body) {
          _this33[name] = function () {
            for (var _len11 = arguments.length, args = Array(_len11), _key11 = 0; _key11 < _len11; _key11++) {
              args[_key11] = arguments[_key11];
            }

            body.call.apply(body, [block].concat(args));

            return _this33;
          };
        })(block, methodName, methodBody);
      }
    }
  } catch (err) {
    _didIteratorError14 = true;
    _iteratorError14 = err;
  } finally {
    try {
      if (!_iteratorNormalCompletion14 && _iterator14.return) {
        _iterator14.return();
      }
    } finally {
      if (_didIteratorError14) {
        throw _iteratorError14;
      }
    }
  }

  return _this33;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Select"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Select (options)](#apidoc.element.squel.cls.Select)
- description and source-code
```javascript
function _class30(options) {
  var blocks = arguments.length <= 1 || arguments[1] === undefined ? null : arguments[1];

  _classCallCheck(this, _class30);

  blocks = blocks || [new cls.StringBlock(options, 'SELECT'), new cls.FunctionBlock(options), new cls.DistinctBlock(options), new
 cls.GetFieldBlock(options), new cls.FromTableBlock(options), new cls.JoinBlock(options), new cls.WhereBlock(options), new cls.GroupByBlock
(options), new cls.HavingBlock(options), new cls.OrderByBlock(options), new cls.LimitBlock(options), new cls.OffsetBlock(options
), new cls.UnionBlock(options)];

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class30).call(this, options, blocks));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.SetFieldBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>SetFieldBlock ()](#apidoc.element.squel.cls.SetFieldBlock)
- description and source-code
```javascript
function _class15() {
  _classCallCheck(this, _class15);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class15).apply(this, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.StringBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>StringBlock (options, str)](#apidoc.element.squel.cls.StringBlock)
- description and source-code
```javascript
function _class6(options, str) {
  _classCallCheck(this, _class6);

  var _this8 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class6).call(this, options));

  _this8._str = str;
  return _this8;
}
```
- example usage
```shell
...
  return this._p;
};


// pragma query builder
var PragmaQuery = function(options) {
  squel.cls.QueryBuilder.call(this, options, [
      new squel.cls.StringBlock(options, 'PRAGMA'),
      new CommandBlock(),
      new ParamBlock()
  ]);
};
util.inherits(PragmaQuery, squel.cls.QueryBuilder);
...
```

#### <a name="apidoc.element.squel.cls.TargetTableBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>TargetTableBlock ()](#apidoc.element.squel.cls.TargetTableBlock)
- description and source-code
```javascript
function _class9() {
  _classCallCheck(this, _class9);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class9).apply(this, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.UnionBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>UnionBlock (options)](#apidoc.element.squel.cls.UnionBlock)
- description and source-code
```javascript
function _class28(options) {
  _classCallCheck(this, _class28);

  var _this32 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class28).call(this, options));

  _this32._unions = [];
  return _this32;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.Update"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>Update (options)](#apidoc.element.squel.cls.Update)
- description and source-code
```javascript
function _class31(options) {
  var blocks = arguments.length <= 1 || arguments[1] === undefined ? null : arguments[1];

  _classCallCheck(this, _class31);

  blocks = blocks || [new cls.StringBlock(options, 'UPDATE'), new cls.UpdateTableBlock(options), new cls.SetFieldBlock(options),
new cls.WhereBlock(options), new cls.OrderByBlock(options), new cls.LimitBlock(options)];

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class31).call(this, options, blocks));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.UpdateTableBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>UpdateTableBlock ()](#apidoc.element.squel.cls.UpdateTableBlock)
- description and source-code
```javascript
function _class10() {
  _classCallCheck(this, _class10);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class10).apply(this, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.WhereBlock"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>WhereBlock (options)](#apidoc.element.squel.cls.WhereBlock)
- description and source-code
```javascript
function _class24(options) {
  _classCallCheck(this, _class24);

  return _possibleConstructorReturn(this, Object.getPrototypeOf(_class24).call(this, _extend({}, options, {
    verb: 'WHERE'
  })));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.isSquelBuilder"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>isSquelBuilder (obj)](#apidoc.element.squel.cls.isSquelBuilder)
- description and source-code
```javascript
function isSquelBuilder(obj) {
  return obj && !!obj._toParamString;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.cls.registerValueHandler"></a>[function <span class="apidocSignatureSpan">squel.cls.</span>registerValueHandler (type, handler)](#apidoc.element.squel.cls.registerValueHandler)
- description and source-code
```javascript
registerValueHandler = function (type, handler) {
  _registerValueHandler(cls.globalValueHandlers, type, handler);
}
```
- example usage
```shell
...
### Custom value types

By default Squel does not support the use of object instances as field values. Instead it lets you tell it how you want
specific object types to be handled:

'''javascript
// handler for objects of type Date
squel.registerValueHandler(Date, function(date) {
return date.getFullYear() + '/' + (date.getMonth() + 1) + '/' + date.getDate();
});

squel.update().
.table('students')
.set('start_date', new Date(2013, 5, 1))
.toString()
...
```



# <a name="apidoc.module.squel.flavours"></a>[module squel.flavours](#apidoc.module.squel.flavours)

#### <a name="apidoc.element.squel.flavours.mssql"></a>[function <span class="apidocSignatureSpan">squel.flavours.</span>mssql (_squel)](#apidoc.element.squel.flavours.mssql)
- description and source-code
```javascript
mssql = function (_squel) {
  var cls = _squel.cls;

  cls.DefaultQueryBuilderOptions.replaceSingleQuotes = true;
  cls.DefaultQueryBuilderOptions.autoQuoteAliasNames = false;
  cls.DefaultQueryBuilderOptions.numberedParametersPrefix = '@';

  _squel.registerValueHandler(Date, function (date) {
    return '\'' + date.getUTCFullYear() + '-' + (date.getUTCMonth() + 1) + '-' + date.getUTCDate() + ' ' + date.getUTCHours() + ':' +
date.getUTCMinutes() + ':' + date.getUTCSeconds() + '\'';
  });

  //�LIMIT,  OFFSET x and TOP x
  cls.MssqlLimitOffsetTopBlock = function (_cls$Block14) {
    _inherits(_class34, _cls$Block14);

    function _class34(options) {
      _classCallCheck(this, _class34);

      var _this39 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class34).call(this, options));

      _this39._limits = null;
      _this39._offsets = null;

      // This is setup as one block to return many as they all have to use each others data at different times
      // The build String of EITHER LIMIT OR TOP should execute, never both.

<span class="apidocCodeCommentSpan">      /**
      # Set the LIMIT/TOP transformation.
      #
      # Call this will override the previously set limit for this query. Also note that Passing 0 for 'max' will remove
      # the limit.
      */
</span>      var _limit = function _limit(max) {
        max = this._sanitizeLimitOffset(max);
        this._parent._limits = max;
      };

      _this39.ParentBlock = function (_cls$Block15) {
        _inherits(_class35, _cls$Block15);

        function _class35(parent) {
          _classCallCheck(this, _class35);

          var _this40 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class35).call(this, parent.options));

          _this40._parent = parent;
          return _this40;
        }

        return _class35;
      }(cls.Block);

      _this39.LimitBlock = function (_this39$ParentBlock) {
        _inherits(_class36, _this39$ParentBlock);

        function _class36(parent) {
          _classCallCheck(this, _class36);

          var _this41 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class36).call(this, parent));

          _this41.limit = _limit;
          return _this41;
        }

        _createClass(_class36, [{
          key: '_toParamString',
          value: function _toParamString() {
            var str = "";

            if (this._parent._limits && this._parent._offsets) {
              str = 'FETCH NEXT ' + this._parent._limits + ' ROWS ONLY';
            }

            return {
              text: str,
              values: []
            };
          }
        }]);

        return _class36;
      }(_this39.ParentBlock);

      _this39.TopBlock = function (_this39$ParentBlock2) {
        _inherits(_class37, _this39$ParentBlock2);

        function _class37(parent) {
          _classCallCheck(this, _class37);

          var _this42 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class37).call(this, parent));

          _this42.top = _limit;
          return _this42;
        }

        _createClass(_class37, [{
          key: '_toParamString',
          value: function _toParamString() {
            var str = "";

            if (this._parent._limits && !this._parent._offsets) {
              str = 'TOP (' + this._parent._limits + ')';
            }

            return {
              text: str,
              values: []
            };
          }
        }]);

        return _class37;
      }(_this39.ParentBlock);

      _this39.OffsetBlock = function (_this39$ParentBlock3) {
        _inherits(_class38, _this39$ParentBlock3);

        function _class38() {
          _classCallCheck(this, _class38);

          return _possibleConstructorReturn(this, Object.getPrototypeOf(_class38).apply(this, arguments));
        }

        _createClass(_class38, [{
          key: 'offset',
          value: function offset(start) {
            this._parent._offsets = this._sanitizeLimitOffset(start);
          }
        }, {
          key: '_toParamString',
          value: function _toParamString() {
            var str = "";

            if (this._parent._ ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.flavours.mysql"></a>[function <span class="apidocSignatureSpan">squel.flavours.</span>mysql (_squel)](#apidoc.element.squel.flavours.mysql)
- description and source-code
```javascript
mysql = function (_squel) {
  var cls = _squel.cls;

  // ON DUPLICATE KEY UPDATE ...
  cls.MysqlOnDuplicateKeyUpdateBlock = function (_cls$AbstractSetField3) {
    _inherits(_class46, _cls$AbstractSetField3);

    function _class46() {
      _classCallCheck(this, _class46);

      return _possibleConstructorReturn(this, Object.getPrototypeOf(_class46).apply(this, arguments));
    }

    _createClass(_class46, [{
      key: 'onDupUpdate',
      value: function onDupUpdate(field, value, options) {
        this._set(field, value, options);
      }
    }, {
      key: '_toParamString',
      value: function _toParamString() {
        var options = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];

        var totalStr = "",
            totalValues = [];

        for (var i = 0; i < this._fields.length; ++i) {
          totalStr = _pad(totalStr, ', ');

          var field = this._fields[i];

          var value = this._values[0][i];

          var valueOptions = this._valueOptions[0][i];

          // e.g. if field is an expression such as: count = count + 1
          if (typeof value === 'undefined') {
            totalStr += field;
          } else {
            var ret = this._buildString(field + ' = ' + this.options.parameterCharacter, [value], {
              buildParameterized: options.buildParameterized,
              formattingOptions: valueOptions
            });

            totalStr += ret.text;
            totalValues.push.apply(totalValues, _toConsumableArray(ret.values));
          }
        }

        return {
          text: !totalStr.length ? "" : 'ON DUPLICATE KEY UPDATE ' + totalStr,
          values: totalValues
        };
      }
    }]);

    return _class46;
  }(cls.AbstractSetFieldBlock);

  // INSERT query builder.
  cls.Insert = function (_cls$QueryBuilder9) {
    _inherits(_class47, _cls$QueryBuilder9);

    function _class47(options) {
      var blocks = arguments.length <= 1 || arguments[1] === undefined ? null : arguments[1];

      _classCallCheck(this, _class47);

      blocks = blocks || [new cls.StringBlock(options, 'INSERT'), new cls.IntoTableBlock(options), new cls.InsertFieldValueBlock
(options), new cls.InsertFieldsFromQueryBlock(options), new cls.MysqlOnDuplicateKeyUpdateBlock(options)];

      return _possibleConstructorReturn(this, Object.getPrototypeOf(_class47).call(this, options, blocks));
    }

    return _class47;
  }(cls.QueryBuilder);

  // REPLACE query builder.
  cls.Replace = function (_cls$QueryBuilder10) {
    _inherits(_class48, _cls$QueryBuilder10);

    function _class48(options) {
      var blocks = arguments.length <= 1 || arguments[1] === undefined ? null : arguments[1];

      _classCallCheck(this, _class48);

      blocks = blocks || [new cls.StringBlock(options, 'REPLACE'), new cls.IntoTableBlock(options), new cls.InsertFieldValueBlock
(options), new cls.InsertFieldsFromQueryBlock(options)];

      return _possibleConstructorReturn(this, Object.getPrototypeOf(_class48).call(this, options, blocks));
    }

    return _class48;
  }(cls.QueryBuilder);

  _squel.replace = function (options, blocks) {
    return new cls.Replace(options, blocks);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.squel.flavours.postgres"></a>[function <span class="apidocSignatureSpan">squel.flavours.</span>postgres (_squel)](#apidoc.element.squel.flavours.postgres)
- description and source-code
```javascript
postgres = function (_squel) {
  var cls = _squel.cls;

  cls.DefaultQueryBuilderOptions.numberedParameters = true;
  cls.DefaultQueryBuilderOptions.numberedParametersStartAt = 1;
  cls.DefaultQueryBuilderOptions.autoQuoteAliasNames = false;
  cls.DefaultQueryBuilderOptions.useAsForTableAliasNames = true;

  cls.PostgresOnConflictKeyUpdateBlock = function (_cls$AbstractSetField4) {
    _inherits(_class49, _cls$AbstractSetField4);

    function _class49() {
      _classCallCheck(this, _class49);

      return _possibleConstructorReturn(this, Object.getPrototypeOf(_class49).apply(this, arguments));
    }

    _createClass(_class49, [{
      key: 'onConflict',
      value: function onConflict(index, fields) {
        var _this56 = this;

        this._dupIndex = this._sanitizeField(index);

        if (fields) {
          Object.keys(fields).forEach(function (key) {
            _this56._set(key, fields[key]);
          });
        }
      }
    }, {
      key: '_toParamString',
      value: function _toParamString() {
        var options = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];

        var totalStr = "",
            totalValues = [];

        for (var i = 0; i < this._fields.length; ++i) {
          totalStr = _pad(totalStr, ', ');

          var field = this._fields[i];

          var value = this._values[0][i];

          var valueOptions = this._valueOptions[0][i];

          // e.g. if field is an expression such as: count = count + 1
          if (typeof value === 'undefined') {
            totalStr += field;
          } else {
            var ret = this._buildString(field + ' = ' + this.options.parameterCharacter, [value], {
              buildParameterized: options.buildParameterized,
              formattingOptions: valueOptions
            });

            totalStr += ret.text;
            totalValues.push.apply(totalValues, _toConsumableArray(ret.values));
          }
        }

        return {
          text: this._dupIndex ? 'ON CONFLICT (' + this._dupIndex + ') DO ' + (!totalStr.length ? "NOTHING" : 'UPDATE SET ' + totalStr
) : '',
          values: totalValues
        };
      }
    }]);

    return _class49;
  }(cls.AbstractSetFieldBlock);

  // RETURNING
  cls.ReturningBlock = function (_cls$Block18) {
    _inherits(_class50, _cls$Block18);

    function _class50(options) {
      _classCallCheck(this, _class50);

      var _this57 = _possibleConstructorReturn(this, Object.getPrototypeOf(_class50).call(this, options));

      _this57._fields = [];
      return _this57;
    }

    _createClass(_class50, [{
      key: 'returning',
      value: function returning(field) {
        var alias = arguments.length <= 1 || arguments[1] === undefined ? null : arguments[1];
        var options = arguments.length <= 2 || arguments[2] === undefined ? {} : arguments[2];

        alias = alias ? this._sanitizeFieldAlias(alias) : alias;
        field = this._sanitizeField(field);

        // if field-alias combo already present then don't add
        var existingField = this._fields.filter(function (f) {
          return f.name === field && f.alias === alias;
        });
        if (existingField.length) {
          return this;
        }

        this._fields.push({
          name: field,
          alias: alias,
          options: options
        });
      }
    }, {
      key: '_toParamString',
      value: function _toParamString() {
        var options = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];
        var queryBuilder = options.queryBuilder;
        var buildParameterized = options.buildParameterized;


        var totalStr = '',
            totalValues = [];

        var _iteratorNormalCompletion18 = true;
        var _didIteratorError18 = false;
        var _iteratorError18 = undefined;

        try {
          for (var _iterator18 = this._fields[Symbol.iterator](), _step18; !(_iteratorNormalCompletion18 = (_step18 = _iterator18
.next()).done); _iteratorNormalCompletion18 = true) {
            var field = _step18.value;

            totalStr = _pad(totalStr, ", " ...
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
