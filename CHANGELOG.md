# CHANGELOG

## 2.6.16
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
