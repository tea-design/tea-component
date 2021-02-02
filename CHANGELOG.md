# CHANGELOG

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
