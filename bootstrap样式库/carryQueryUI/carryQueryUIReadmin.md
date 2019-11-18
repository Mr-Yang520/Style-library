# carryQueryUI 全局样式说明文档

## 清空默认样式

## 布局

.container 设置为容器：水平方向居中。宽度部位 100% 左右内边距为 15px 高度没有
.container-fluid 宽度为 100% 的容器 没有外编辑；内边距左右 15px 上下 0px 没高度

## 按钮 -btn

#### 普通的按钮样式

成功 btn-success
f 警告 btn-warning
错误 btn-error
取消 btn-cancel
确认 btn-sure
默认 btn-default
危险 btn-danger
首选 btn-primany
一般信息 btn-info
百搭按钮 btn-normal
暖色按钮 btn-warm

#### 渐变的按钮样式

成功 btn-success-rgb
f 警告 btn-warning-rgb
错误 btn-error-rgb
取消 btn-cancel-rgb
确认 btn-sure-rgb
默认 btn-default-rgb
危险 btn-danger-rgb
首选 btn-primany-rgb
一般信息 btn-info-rgb
百搭按钮 btn-normal-rgb
暖色按钮 btn-warm-rgb

#### 伪类按钮样式

- 型号
  大 btn-bg
  小 btn-sm
  中 btn-md

- 圆角按钮 btn-radius

## 表单

## 滑块

## selec 选择框

## 表格 .table

.table 表示基础表格；必须在 table 标签中使用；表示只有列边框的表格
.table-striped 表示条状表格；表体的偶数行；有一定的背景颜色
.table-column 表示半边框样式
.table-hover 表示悬浮表格
.table-condensed 紧缩表格
.table-border 边框表格
.table-inverse 背景色为黑色的表格
.table-inverse-striped 黑色条形表格
.table-inverse-hover 黑色悬浮样式 需要依赖 .table-inverse 或者 .table-inverse-striped
.table-contrl 表示【控制列】 固定；其他列可以滚动 .table-control 必须给 table 标签的祖籍元素添加；而不是给父元素添加 .table-box 表示 table 的父容器

```css
.table-contrl {
  position: relative;
}
.table-contrl table > tr > td:last-child {
  position: absolute;
  right: 0;
  min-width: 120px;
  text-align: center;
  box-shadow: -5px 4px 6px 1px #ccc;
}
/* 选中导入第二列；解决内容遮罩问题 */
.table-contrl table > tr > td:nth-last-child(2)::before {
  content: "";
  width: 120px;
}
.table-contrl > .table-box {
  overflow: auto;
}
```

.table-responsive 移动端表格；可以有横向滚动的效果. .table-responsive 需要给 table 的父容器添加

状态表格；给 tr 添加类名
.success 成功
.info 通过
.waring 警告
.danger 危险
.primary 首选
.warm 暖色

## 栅格系统

## 分页 .Page

.pagination 实现分页样式。有 ul li a 完成的分页效果
.pagination-bgc 表示带有背景颜色的分页
.pagination-noBgc 表示没有背景颜色的分页
.pagination-inverse 黑色的分页 #393d49

## 表单类

### 单选多选框样式

.circle-check 圆形选择框 .circle-check 需要给 input[type=checkbox]的付元素添加
.square-check 正方形选择框 .square-check 需要给 input[type=checkbox]的付元素添加

```html
<!-- 示例代码 -->
<div class="circle-check">
  <input type="checkbox" />
</div>
<div class="square-check">
  <input type="checkbox" />
</div>
```

### 滑块 .sliderbar
.slider-wrap 表示进度条外围容器
.sliderbar 表示 滑块的条
.sliderbar-control 表示控制键

```html
  <div class="slider-wrap">
      <div class="sliderbar">
        <div class="sliderbar-control">
          55
        </div>
      </div>
    </div>
```
状态
.sliderbar-success
.sliderbar-info
.sliderbar-primary
.sliderbar-error

### 开关 .switch
.switch 开关样式的选择框  需要给  input[type=checkbox class=switch] 才能实现效果  
      - 绿色我开 input = checked  灰色为关  input = disable
 状态
 .switch-info  蓝色开 灰关
 .switch-danger  红开 灰关
 .switch-warm 橙开 灰关
 .switch-primary  蓝开 红关 
 
### 步骤组件 
.step-wrap 为 外部容器  55rem
.step-full  每个步骤容器  包含内容 ；圈 线  文本
.step-line-box 具体进行的每一步。用 Input[type = checkbox], 当有 checked 属性表示当前步骤已经完成。
.step-circle 表示 圈 
.step-line 表示 线
.step-text 表示步骤内容

状态 
.step-circle-info
.step-circle-success
.step-circle-primary
.step-circle-warm
.step-circle-error
.step-circle-danger 

### 导航 .nav
注意：导航仅仅适用于 pc 端应用；且只使用与静态的样式，导航中所有的样式都是操作li下a 标签
.nav-tab 表示 tab 样式的导航条  需要依赖 .nav
.nav-pills 胶囊式的导航   需要依赖.nav
.nav-stacked  侧边导航栏  需要依赖.nav


.nav-inverse 表示背景色为黑色的导航
.nav-aside  表示侧边栏导航
.nav-fixed-top 表示固定导航 在顶部
nav-fixed-left 表示 屏幕左边固定导航
.nav-fixed-right  表示 屏幕右边固定导航



### 导航条  .navbar
兼容移动端样式设置规则：媒体查询最小宽度；写pc端样式；当小于这个宽度时候；使用浏览器默认样式
网站的导航条；到移动端时候可以折叠 

.navbar  导航条 兼容pc 移动  默认样式为隐藏状态
.navbar-default 给导航条【添加样式】 背景色
.navbar-header 有媒体查询样式；做PC 端和移动端区分； 移动端宽度100%
.collapse  元素隐藏[移动端]
.nav-collapse.collapse 在pc 端【强制】显示
.navbar-nav 表示导航条下导航
.navbar-form 表示导航条中输入框
.navbar-left 让导航在导航条中左浮动【移动端无浮动】
.navbar-right 让导航有又浮动【移动端无浮动效果】
.navbar-toggle 表示显示隐藏列表导航栏，有【右浮动】效果

.navbar-fixed-top 固定顶部导航条
.navbar-inverse 黑色导航条 border-bottom:1px solid black
   .navbar .active  背景颜色黑色  字体白色

 .breadcrumb 表示路径导航；没有基础类  

  - 每个a 添加伪元素； content:"Z/\00a0".navbar 导航条 兼容移动  默认样式 【隐藏】



## 规范：

1：清空所有 Html 标签的默认样式

2：字体：标准 14px 最大 36px 最小 12 px

3: 布局 栅格系统 ：给一一个父容器 等分多少份?
12 列：
每个子元素可以占 12 列中 1-12 最大为 12 分
col-12 占据 12 份



### 表单样式组件
1：只有表单样式。分为基础样式与可选择样式。如有特殊需要；请自定义
2：表单没有进行验证处理。有对验证效果样式处理；statice 状态。
3：表单验证需要JS  正则完成。 注意：正则规则必须写基础正则不要写新的正则 因为 IE 和火狐部分版本不兼容
##### 表单组件基础样式：
.form-group 表示 表单组件
.form-control 表示表单控件
.form-label 表示input 的提示信息只能应用在 label 标签中

##### 可选项表单样式
.form-inline 表示横向的表单 表
.form-horizontal 纵向表单

##### 表单中控件
.form-check 选择项组件 在ul 中是使用
.form-check-item  表示多选项  在li 中使用
.check-content 表示 选择的文本描述


### 栅格系统 .col
栅格系统 是横向布局的处理 
提示 如果 父容器；不适用.row  那么自己清楚浮动；计算父容器高度

#### 容器 .row
将.row 容器等分为12 份
#### 屏幕
.col-xs-xx  768 以下尺寸
.col-sm-xx   768以上 992以下
.col-md-xx   992 以上   1200 以下
.col-lg-xx   1200 以上



#### 分的份数  小数点 后 7位数
1- 8.33333333%
2- 16.6666667
3- 25
4- 33.3333333
5-41.6666667
6- 50
7- 58.3333333
8- 66.6666667
9- 75
10-83.3333333
11-91.6666667
12-100


#### 列偏移
通过改变 positon:relative  Left  实现列偏移
*表示 1 2 3 4 5 6 7 8 9 10 11 12
.col-xs-offset-*
.col-sm-offset-*
.col-md-offset-*
.col-lg-offset-*
##### 偏移量
1
2
3
4
5
6
7
8
9
10
11
12

#### 排列
.col-xs-pull-* 相对元素位置右边多元（往左走）
.col-xs-push*   往右边走









### 开发浏览器注意事项
1： 如果您是 ie7 8 请您更换浏览器
2： IE7 尽量全部使用 div  例如
   - ul   div.ul  
   - li  div.li   
   - span  div.span 设置 display: inline  
3: ie78 不支持 浮动 清楚浮动  css3 百分之90属性