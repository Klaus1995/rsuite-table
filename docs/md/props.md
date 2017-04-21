

#### `<Table>`

Name | Type | Default | Description |
---- | ---- | ------- | ----------- |
data `isRequired` | Array |  |  表格数据
width | number | | 宽度
height | number | 200 | 高度
rowHeight | number | 36 | 行高
headerHeight | number | 36 | 表头高度
isTree | bool | | 是否展示为树表格
expand | bool | | 展开所有节点，`isTree`为 `tree` 时，改值有效
locale | object |  | 本地化语言配置
sortColumn | string |  | 排序列名称
sortType | string |  | 排序类型  ['desc', 'asc']
onRowClick | func  |  | 行点击后的回调函数， 返回 `rowDate`
onSortColumn | func  |  | 点击排序列的回调函数，返回 `sortColumn`, `sortType` 这两个值

<br>
####  `<Column>`

Name | Type | Default | Description |
---- | ---- | ------- | ----------- |
align | string |  |  对齐方式 ['left', 'center', 'right']
width | number | | 列宽
fixed | bool |  | 固定列
resizable | bool |  | 可自定义调整列宽
sortable | bool |  | 可排序
flexGrow | number | | 设置列宽自动调节的比例，当设置了 `flexGrow` 就不能设置 `resizable` 与 `width` 属性
<br>
> `sortable` 是用来定义该列是否可排序，但是根据什么 `key` 排序需要 在 `Cell` 设置一个 `dataKey`
> 这里的排序是服务端排序，所以需要在 `<Table>` 的 `onSortColumn` 回调函数中处理逻辑，回调函数会返回 `sortColumn`, `sortType` 这两个值。

<br>
####  `<Cell>`

Name | Type | Default | Description |
---- | ---- | ------- | ----------- |
dataKey | string |  |  数据绑定的 `key` ，同时也是排序的 `key`
align | string |  |  对齐方式 ['left', 'center', 'right']
rowData | object |  | 行数据
rowIndex | number |  | 行号