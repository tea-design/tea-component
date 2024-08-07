# CHANGELOG

## 2.8.0
`2024-07-18`

 <img src="https://github.com/user-attachments/assets/b0daee67-3546-462c-85f3-c009ed962f97" width="84" />
 
#### 升级必读

🌟 新的样式方案使用了 CSS 变量，你需要引入一个主题以及新的样式文件：

- 从 `tea-component/dist/themes/` 下选择主题引入
- 把 `tea-component/dist/tea.css` 替换为 `tea-component/dist/tea-themeable.css`

#### 主要变化
- 💄 全新的 UI 视觉风格，更轻量、 更高效的视觉传达，引入更高辨识度的线性图标库
- 💄 全新的主题方案，支持多主题和深浅模式
- 🌟 新增 Space 组件，轻松设置组件间距与对齐方式
- 🔥 新增独立图标库，支持自定义尺寸和颜色
- Theme
	- 🔥 支持在 JS 中使用 CSS 变量
	- 🔥 支持独立配置指区块的 Theme Mode
- InputNumber 
	- 🐞 InputNumber 组件设置 allowEmpty 属性后，value 从 null 变成 有值（100）时，输入框不显示值的问题
- ImagePreview
	- 🆕 ImagePreview 组件支持传入 img 元素的原生属性 
- Table
	-  🐞 修复当 table 存在 fixed 列时，resizable 插件宽度计算有误的问题
	 - 🐞 修复表头文字截断异常等问题
	- 💄 优化表头图标对齐方式
	- 💄 优化表格横向滚动时，状态内容（autotip）居中显示
	- 🪄 重构部分实现以提高渲染性能
- FormItem
	-  🆕 增加 `tipsClassName` 和 `tipsStyle` 属性控制 tips 样式  
- Tag
	- 🆕 新增属性 `shapeType` `variant` `size` `before` `after`
	- 🗑 废弃属性 `dark` `bordered`
- TimePicker
	- 🐞 修复传入value 超出限制直接点确认无法设置所选时间
- SearchBox
	- 🆕 新增属性 `iconPlacement`
- List
	- 🆕 `type` 属性值新增 `plain`
	- 🆕 新增子组件`List.ItemButton` `List.ItemDecorator` `List.ItemContent` `List.SearchBox` `List.ListDivider`等
	- 🆕 新增 9 个 List 的使用场景
	- 💄 `List.Item` 高度由 30px 调整为 **32px**
- TagSearchbox
	- 💄 对 TagSearchbox 单独实现的类似 Tag 组件的 className 调整成和 Tag 组件进行统一，尽量确保表现一致
- Card
	- 💄 调整边框、投影、hover 状态样式
	- 💄 调整 Card.Body 内间距、标题字号
- Datepicker
	- 💄 区间选择，宽度由 200px 调整为 **220px**
	- 💄 包含时间的区间选择，宽度由 300px 调整为 **325px**
	- 💄 包含毫秒的区间选择，宽度由 350px 调整为 **360px**
- Checkbox & Radio
	- 💄 `tea-form-check__label` 布局调整为 `inline-flex` 布局


---

## 2.7.9
`2023-03-13`

- Drawer 样式层级调整

## 2.7.8
`2022-09-29`

- **移除了组件及样式文件中的 CDN 文件链接**
- Table 滚动插件新增 `scrollToBottomOnChange` 属性支持变化后滚动至底部
- 修复浮层类组件在 Safari 下可能出现的闪动问题
- 优化 Blank 组件样式，内置主题升级至新的视觉版本
- 优化 TagSearchBox 帮助提示，将图片转换换为表格实际渲染


## 2.7.7
`2022-09-22`
- 新增 Avatar 头像组件
- TagSelect 新增 `removeable` 属性
- Table 虚拟滚动新增 `updateDeps` 属性支持强制刷新
- Select 多选新增 `onlySubmitFilterFromAll` 属性只全选过滤后的字段
- Tree 事件 `onSelect` 增加 `nodeContent` 参数
- Tree 组件虚拟滚动支持更多属性
- RegionOption 组件支持自定义类名属性
- Copy 支持修改覆盖层样式
- RangPicker 支持分组 placeholder 设置
- TimeRangePicker 支持清空
- 修复 Table 组件开启固定列可能导致的性能问题
- 修复 Table 组件 ResizeObserver 没有清理的问题
- 修复 RangePicker 设置不同日期同一时间 range 后无法选择问题
- 修复 TimePicker 可能出现的 topOption 元素不存在报错问题
- 修复 DatePicker 时间组件样式问题
- 优化 AutoComplete 弹出层动画
- 优化 InputPassword tabindex 聚焦
- 优化 RangPicker 样式

## 2.7.6
`2022-06-20`
- 修复 DatePicker 组件偶尔出现无法切换日期面板问题

## 2.7.5
`2022-06-17`
- 修复 DatePicker 组件 value 为空报错的问题

## 2.7.4
`2022-06-09`
- Table 列宽度调整插件 新增支持单行
-  Cascader data 的 label 新增支持 `ReactNode`
-  TimePicker 新增毫秒级别，新增输入修改时间
-  DatePicker RangePicker 新增季度 月份选择，新增毫秒级别，新增输入修改日期
-  TagSearchBox 新增删除tag的 `onTagDelete`事件
-  Upload 新增支持在 `beforeUpload` 转换文件
-  Guide 样式优化
-  ImagePreview 增加 Modal `ClassName` 透传
- 修复 Drawer 切换后组件内容没变化

## 2.7.3

`2021-12-16`

- Slider 新增多段及点选择模式
- TagSelect 新增 `hideCloseButton` 属性
- Table 拖拽新增 `onDragStart` 事件
- Tree 支持点击和展开时回调当前节点数据
- Menu 项图标配置支持自定义节点
- SelectMultiple 无 `options` 时显示 `value`
- 修复 InputNumber 在 `allowEmpty` 时初始值不生效的问题
- 修复 TagSearchBox 值选择框可能溢出可视范围的问题
- 修复 TagSelect 设置 `footer` 时无法点击的问题
- 修复 TagSelect 键盘选择问题
- 修复 Tree 操作区域点击冒泡
- 修复 RegionSelect 缓存报错及数字 0 展示问题

---

## 2.7.2

`2021-11-08`

- 修复 Tree 多层自定义节点无法渲染的问题
- 优化 Table selectable 插件 `onChange` 中 `context` 字段的数据
- 优化 RegionSelect `shortcut` 属性使用

---

## 2.7.1

`2021-11-03`

- 修复 Table 拖拽排序报错的问题
- 修复 Alert 轮播缺失 key 产生 warning 的问题

---

## 2.7.0  ⭐

`2021-11-01`

- 新增 Rate 组件
- 新增 Timeline 组件
- Tree
	- **渲染结构更新，节点铺平渲染**
	- 新增 `height` 属性支持开启虚拟滚动以提升大数据时性能
	- 新增 `selectValueMode` 属性支持选中值格式配置
	- 新增 `defaultExpandAll` \/ `defaultExpandParent` \/ `forceExpandParent` 属性支持展开控制
	- 新增 `fullActivable` 属性支持整个节点范围点击可控制高亮
- Select
  - **聚焦/失焦行为优化，列表项不再响应 `onFocus` 事件**
  - **移除 `type` 属性，原有设置 `type="native"` 的组件保留支持原生下拉样式，其他转为模拟下拉**
  - 新增 `virtual` 属性，支持关闭虚拟滚动，关闭后下拉列表宽度可自适应内容宽
  - 新增 `matchButtonWidth` 属性支持设置下拉列表与下拉按钮同宽
- Tabs
	- **样式优化，`addon` 区域布局样式更新**
	- 新增 `activeTabAutoScrollIntoView` 属性支持配置自动滚动到当前项的行为
	- 修复宽度变化时滚动状态未重置的问题
- Table
  - **虚拟滚动 scrollable 及多选 selectable 插件重构以提升大数据时性能**
  - 修复 draggable 插件拖起行某些场景下宽度不正确的问题
  - 修复 selectable 变更回调 `context` 中 `check.value` 可能相反的问题
- InputNumber
	- 新增 `formatter` / `parser` 属性支持格式化显示
	- 新增 `allowEmpty` 属性允许使用空值
	- 新增 `inputProps` 支持设置输入框属性
- TagSelect
  - 新增 `footer` 属性支持配置尾部内容
  - 默认 `value` 选中被禁用的项时对应标签不显示关闭按钮
  - 聚焦失焦行为优化，下拉列表不再响应 mousedown 及 focus 事件
- Cascader
 - 新增 `valueMode` / `showMode` 属性支持值格式及展示模式配置
 - 修复开启搜索后 `disabled` 不生效的问题
- Text
  - 支持 `tooltip` 传递 boolean 值以提示与原文相同内容
  - 修复 `copyable` 和 `overflow` 无法同时使用的问题
- SearchBox
	- 新增 `searchBoxRef` 参数执行外层容器
	- 修复禁用时按钮仍可点击的问题 
- Grid 支持响应式栅格
- TagSearchbox 自定义值选择器渲染新增 `onOperationalKeyDown` 属性支持监听部分按键事件
- Collapse 新增 `destroyInactivePanel` 支持销毁未激活面板
- 浮层类组件新增 `flipped` 属性支持配置距离可视范围空间不足时是否翻转方向
- 修复 Menu 组件收起状态样式在 Safari 下异常的问题
- 修复 TimePicker `clearable` 属性不生效的问题
- 修复 TimePicker 键盘事件无响应的问题
- 修复 Upload 获取 `action` 失败时异常未捕获的问题
- 修复 Password 禁用和只读状态
- 修复 Alert 轮播包含空元素时的行为
- 浮层类组件自定义 `trigger` 类型优化

---

## 2.6.22
`2021-06-01` 😋

- 修复 Table 下 draggable / columnsDraggable 拖拽插件浏览器兼容问题
	- 在 QQ 浏览器下无法使用
	- 在 FireFox 下拖拽导致打开新页面
- 修复 Table 按路径切割 key 获取值时值不存在导致报错的问题
- 修复 Cascader 选中值包含非字符串 `label` 时展示异常的问题
- 修复 Switch 点击时 `onClick` 事件被触发多次的问题
- 优化 AutoComplete 组件类型，类型上兼容包裹非 Input 组件
- 根目录直接导出 TextArea 组件

---

## 2.6.21
`2021-05-24`

- Table key 相关属性 `.` 路径切割兼容原有包含 `.` 的字符串 key（整体 key 值不存在时再进行切割遍历）
```
如 `recordKey` 设置为 `"info.name"` 时：
优先读取 `record["info.name"]`，该值不存在时读取 `record.info.name`
```
- 修复 Table 不传 `records` 时报错的问题（2.6.19 引入）
- 修复 Select unmount 时可能产生 warning 的问题


---

## 2.6.20
`2021-05-20` ❤️

- 修复 StatusTip 样式问题（2.6.19 引入）
- 修复 ListSubMenu unmount 时可能产生 warning 的问题

---

## 2.6.19
`2021-05-19`

- 升级相关依赖解决 npm install 出现的 react 17 peerDependencies 异常
- ImagePreview 新增 `maskClosable` 属性
- 修复 Dropdown/Select `onFocus` 失效的问题
- 修复 Select 顶部使用 ErrorTip 过长时未展示的问题
- 修复移动端 Select 搜索无法点开的问题
- 修复 Table 无数据时表头固定列失效
- 修复 Transition 退出动画未结束时更新 children 进入内容未更新问题
- 修复 Switch 切换动画未生效的问题
- Pagination 总数为 0 时不触发 pageCountChangingReset
- Pagination 页码输入支持失焦时生效

---

## 2.6.18
`2021-05-17`

- Guide 新增 `nextButtonTheme` 属性支持下一步按钮样式配置
- Guide 步骤新增 `scrollIntoViewOptions` 属性支持单步骤自动滚动位置控制
- Table draggable 内置版本与第三方版本行为/属性对齐
- 修复 Select `listWidth` 小于样式 minWidth 时无效的问题
- 移除 ImagePreview 外层多余层级
- 升级依赖以解决 React 17 peerDependencies 报错

---

## 2.6.17
`2021-04-28`

- 新增 ar 语言包
- Cascader 新增 `valueRender` 属性支持自定义选中值渲染
- ImagePreview 新增 `children` 属性支持自定义触发元素
- 修正浮层类组件多层叠加时的行为（浮层点击内部产生的二级浮层不关闭自身）
- **修复 TagSearchBox 受控状态下无法触发已有选项下拉选择的问题（2.6.14 引入）**
- 修复 Bubble 在 Select 及禁用 Input 上无法弹出的问题
- 修复 Slider 点击标尺文字发生跳转的问题
- 修复 Switch 非 `disabled` 下 `loading` 不生效的问题
- 修复 Layout.Sider 在 Safari 下收起后宽度样式问题
- 补全 NavMenu.Item 各类型 selected 样式

---

## ~~2.6.16~~
`-`

*浮层异常，不要使用该版本*

---

## 2.6.15

`2021-04-20`

- 升级依赖修复 Upload 不合法文件回调报错的问题
- 修复 Cascader `value` 设置为 undefined 报错的问题
- 修复 Table 拖拽插件单元格内容为 [] 时报错的问题

---

## 2.6.14
`2021-04-16`

- Dropdown 新增 `updateDeps` 属性支持定义浮层位置更新的依赖项
- 修复 TagSearchBox 可能出现的内部 ref 获取为 undefined 导致报错的问题
- **修复加入 `forwardRef` 导致的部分组件 `children` 类型报错（2.6.11 引入）**
- **移除了 TagSearchBox 中已 React 废弃的 `componentWillReceiveProps` 生命周期**

---

## 2.6.13
`2021-04-14`

- Table 新增内置行拖拽插件，支持多层表格树形拖拽
- **修复开发模式下可能出现的 Ref 使用报错（2.6.11 引入）**
- 修复 Cascader 动态加载数据场景预先传入 `value` 导致报错的问题
- 修复 TagSearchBox 标签编辑 Tag 时删除全部内容影响其他 Tag 的问题

---

## 2.6.12
`2021-04-12`

- Casader 多选新增 `all` 属性支持全选
- **修复 Table 类型泛型丢失的问题（2.6.11 引入）**
- 修复 Table/Affix 可能产生的卸载后更新
- 修复 TimeRangePicker 初始禁用配置不生效修正的问题
- Casader 无对应数据 `value` 项处理优化

---

## 2.6.11
`2021-04-12`

- **补全全部组件的 `forwardRef`**
- **补全全部组件的 `displayName`**
- 移除组件内部 moment ESM 方式的使用（支持 esbuild 构建）
- 修复 Table 可能产生的卸载后更新
- 优化 Upload 标签使用
- 部分样式优化

---

## 2.6.10
`2021-04-07`

- DatePicker 等时间选择相关组件支持时区（配合 `moment-timezone` ）
- Progress 新增 `strokeColor` / `strokeWidth` / `width` 属性支持自定义样式
- Guide `onCurrentChange` 新增返回 `context` 包含当前步骤切换信息
- Collapse
	- 新增 `accordion` 属性支持手风琴模式
	- 修复嵌套多层使用时面板展开问题
- 修复部分样式问题

---

## 2.6.9
`2021-03-19`

- Dropdown 新增 `openDelay` / `closeDelay` 属性支持开关延迟配置
- Table removeable 插件新增 `targetColumnKey` / `render` 支持自定义列/自定义渲染
- Select `onChange` 回调中 context 中新增 `option` 参数
- **修复 Tree 异步加载下不可展开结点在点击时仍触发 `onLoad` 的问题**
- **修复 Cascader 多选时禁用选项可通过父节点选中的问题**
- 修复 Table draggable 插件拖起行某些场景下宽度不正确的问题
- 修复 InputPassword 设置 `size="full"` 不生效的问题
- 修复 Table 在 IE 下开启虚拟滚动提示区域样式显示异常
- 修复 RegionSelect 无选项时报错

---

## 2.6.8
`2021-03-11`

- Form.Item 新增 `tips` 属性支持对项添加描述提示
- Form.Item 新增 `extra` 属性支持对项添加额外信息（可与 `message` 共存）
- 修复 TagSearchBox 标签内容过长导致出现滚动时组件无法点开的问题
- 修复 SegmentMultiple 选项样式类名不生效的问题
- 修复 Input 意外传递 `children` 导致崩溃的问题
- 修复 InputPassword 组件在 Form 中默认对齐位置不正确的问题
- 补充 Pagination 相关类型导出

---

## 2.6.7
`2021-03-04`

- Table draggable 插件新增 `targetColumnKey` 属性支持指定手柄列
- 修复 Cascader 动态加载切换父级无法刷新的问题
- 修复 Cascader 异步加载模式下搜索报错的问题
- 修复 Tree 无法多节点同时异步展开的问题
- 修复 List.Item 中 `tooltip` 未使用但渲染出结构的问题
- Menu 项 `tag` 样式优化 & 支持传递 Badge 组件
- Input.Password 显示图标优化
- Message 样式定位调整
- 新增部分图标

---

## 2.6.6
`2021-02-22`

- Popover 新增右键触发 `trigger`
- 修复 Table selectable 插件 shift 连选可选中禁用项的问题
- 修复 Table selectable/radioable 插件配合 draggable 插件使用报错的问题
- 修复 Cascader 多选叶结点包含相同 `value` 项导致 key 冲突引发的展示问题
- 修复 Cascader 多选 `data` 缺失已选项对应值时报错的问题
- 修复 Affix `className` 及 `style` 设置层级不正确的问题

---

## 2.6.5
`2021-02-08`

- 修复 Upload 不合法文件回调报错的问题

---

## 2.6.4
`2021-02-06`

- Guide 步骤新增 `hideCount` 属性支持隐藏计数显示
- 修复 Cascader 设置 `style` 不生效的问题（2.6.0 引入）
- 修复 Cascader 传递不存在对应选项的 `value` 时报错的问题
- 补充部分工具方法导出

---

## 2.6.3
`2021-02-02`

- Dropdown / Select 新增 `footer` 属性支持自定义渲染浮层底部内容
- Pagination 新增 `pageCountChangingResetType` 属性支持当页码大于总页数时自动重置当前页码
- Guide 步骤新增 `arrowPointAtCenter` / `placementOffset` 属性支持设置偏移及箭头指向
- 修复 Cascader 在 `"menu"` 模式下菜单列表变化浮层位置未更新的问题
- 修复 Table `recordKey` 取值为数字 0 时被转空字符串的问题
- 优化 Menu 相关组件属性透传以支持气泡包裹

---

## 2.6.2
`2021-01-29`

- 修复 Tooltip 包裹 `disabled` 态 Button 时无法消失的问题（2.6.0 引入）
- 修复 TextArea 在 `showCount` 时 `size="full"` 不生效的问题
- 修复 SearchBox 在 Mac Chrome 下输入法未完成时回车触发 `onSearch` 的问题
- 优化下拉组件键盘交互

---

## 2.6.1
`2021-01-25`

- 修复气泡类组件在边界出现时可能出现漂移的问题（2.6.0 引入）
- 修复 Table `columnsDraggable` / `columnsResizable` 插件结合其他插件使用时 props 未向下透传的问题

---

## 2.6.0 ⭐
`2021-01-22`

- Cascader
  - 新增 `type="menu"` 多级菜单类型级联选择
  - 新增 `searchable` 属性支持搜索
- Table
  - 新增 `columnsDraggable` 列拖拽排序插件
  - 新增 `columnsResizable` 列宽度调整插件
  - `sortable` 插件新增 `sorter` 属性支持自定义单列排序规则
  - `columns` 中 `key` 等支持路径嵌套方式获取值（如 `"a.b.c"`）
  - 修复 `groupable` 插件 `align` 配置未生效问题
- Input
  - 类型定义重构
  - 多行输入由 Input 拆分出 Input.TextArea 以解决类型混合问题
- Upload
  - 新增 `send` 属性支持自定义 XHR send 发送的数据体
  - 修复  `onSuccess` 可能触发两次的问题
- TagSearchbox
  - 支持 ESC 关闭
  - 修复火狐下粘贴多行内容不自动分组的问题
- Dropdown 及浮层组件新增 `destroyOnClose` 属性支持配置浮层消失时是否销毁内容
- 气泡类组件支持同时包裹多层使用
- Copy 支持包裹非 Element 内容
- Drawer 新增 `popupContainer` 支持配置渲染位置
- 修复谷歌翻译导致的异常（[react/issues/11538](https://github.com/facebook/react/issues/11538#issuecomment-390386520)）
- 修复 TagSelect 输入框宽度计算不正确导致 `placeholder`  展示不全的问题
- 修复 DatePicker 包含时间时可能污染源 `value` 的问题
- 修复浏览器放大时 `onScrollBottom` 不触发的问题
- 修复 Pagination 内输入框回车触发表单提交的问题
- 修复 IE 下 getBoundingClientRect 可能产生的未指明的错误
- 修复 IE 下 Modal 闪现消失的样式问题
- 修复气泡包裹禁用态按钮时点击仍会弹出的问题
- 优化组件默认搜索行为，不再区分大小写
- 优化 Modal 中 Form.Action 内按钮显示样式
- 优化部分组件被浮层直接包裹不生效需要额外包一层元素的使用方式
- 补充部分图标
- 补充部分 ARIA 属性

---

## 2.5.6
`2020-12-14`

- 修复 TagSelect 在 `disabled` 时 `placeholder` 不显示的问题
- 修复不同版本组件 Notification 同时使用时可能报错的问题

---

## 2.5.5
`2020-12-10`

- 修复 Modal/Drawer 出现时全局滚动条仍可使用的问题
- 修复 Modal/Drawer 消失后焦点未还原的问题
- 优化 TagSelect/TagSearchbox 在使用输入法输入过程中输入框宽度未撑开的问题（2.5.0 Input 变更引入）

---

## 2.5.4
`2020-12-07`

- Modal 新增 `maskStyle` 属性
- 修复组件浮层在 window 滚动时 `closeOnScroll` 不生效的问题
- 修复 Modal/Drawer 组合使用时点击外部关闭的顺序问题
- 补充 Tooltip `popupContainer` 属性

---

## 2.5.3
`2020-12-02`

- 组件库 `peerDependencies` 兼容 React 17
- Drawer 新增 `showMask` 及 `maskStyle` 属性支持遮罩配置
- 修复 Modal 展开时焦点未移动至弹窗的问题
- 修复 Drawer 展开时焦点未移动至抽屉的问题
- 修复多层 Drawer 叠加时点击外部关闭的顺序问题
- 修复 SliderProps / AffixProps 未导出问题
 
---
 
## 2.5.2
`2020-12-01`

- **组件文字颜色样式覆盖方式优化**
- Message/Notification 支持 `duration` 设置为 0 时不自动关闭

---

## 2.5.1
`2020-11-26`

- **部分新样式优化调整修正**
- Upload 新增 `method` 属性支持 HTTP Method 配置

---

## 2.5.0 ⭐
`2020-11-25`

- **样式**
	- 新增深色主题样式 `tea-dark.css`
    - 样式移动至 `@tencent/tea-component/dist` 目录
    - 默认主题样式优化
- **Input 及涉及输入组件在 `composition` 事件期间将不再触发 `onChange` **（即输入法输入未完成期间不会触发 `onChange`）
- ConfigProvider 及各浮层组件新增 `popupContainer` 属性支持配置弹出节点
- RegionSelect 视觉/结构优化，新增快捷选项配置
- Slider
	- 新增 `rangeMode` 属性支持双端滑块模式
    - 新增 `vertical` 属性支持垂直模式
    - 修复移动端无法拖拽的问题
- Table
	- 新增表头分组插件 `groupable`
    - `selectable` 插件 `rowSelectable` 属性新增返回 record
- Modal
	- 支持全局配置 `Model.config`
    - `Model.alert` 默认加入了关闭按钮
- Select 新增 `listWidth` 属性支持下拉列表宽度配置
- MonthPicker 新增 `disabledMonth` 属性支持禁用月份配置
- Input 多行模式下新增 `showCount` 属性支持展示输入字数
- Notification 新增 `unique` 属性支持多条相同内容通知过滤
- List 下 SubMenu 新增 `visible` 及 `onVisibleChange` 属性支持受控展开
- Cascader
	- 新增项禁用及无数据状态
    - 修复不同面板相同 value 导致 key 冲突的问题
- InputNumber.
	- 新增 `onInputChange` 属性支持控制输入行为
	- 修复初始值非法时报错的问题
    - 修复空值时按下回车重置逻辑与失焦时行为不一致的问题
- Menu 子菜单包含选中项时首次渲染将默认展开
- 修复 SelectMultiple tooltip 内容展示不完整的问题
- 修复 TagSelect 在 `disabled` 时点击触发的 ref 不存在问题
- 修复 TagSearchBox 单选值选择器配置搜索未生效的问题
- 修复部分 SSR 使用报错问题

---

👻
