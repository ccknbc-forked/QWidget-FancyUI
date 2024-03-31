<div align="center">
  <h1>FancyUi - Qt Widget</h1>
</div>


<div align="center">
  <img src="https://img.shields.io/badge/License-GPLv3-green?logoColor=63%2C%20185%2C%2017&label=License&labelColor=63%2C%20185%2C%2017&color=63%2C%20185%2C%2017">
  <img src="https://img.shields.io/badge/Language-C++-rgb(243,75,125)">
  <img src="https://img.shields.io/badge/Language-Python-rgb(53,114,165)">
  <img src="https://img.shields.io/badge/Qt-QMake-rgb(158,106,3)">
  <img src="https://img.shields.io/badge/Qt-Qt%20Widget-63%2C%20185%2C%2017">
</div>
<div align="center">
    <img src="https://img.shields.io/github/stars/BFEMCC/Qt-widget-Fancy_UI?style=default&label=%E2%AD%90%EF%B8%8Fstars">
    <img src="https://img.shields.io/github/forks/BFEMCC/Qt-widget-Fancy_UI?style=default">
    <img src="https://img.shields.io/github/watchers/BFEMCC/Qt-widget-Fancy_UI?style=default">
</div>


<p align="center">
 简体中文 | <a href="./README_EN.md">English</a>
</p>
<h4>
    控件目录
</h4>
<ul>
  <li>按钮
    <ul>
      <li>悬浮填充按钮 • HoverFillButton</li>
    </ul>
  </li>
  <li>其余控件整理中......</li>
</ul>

# 按钮

## 悬浮填充按钮 - HoverFillButton

### GIF示例

<img src="./GIF/HoverFillButton.gif" style="zoom:150%;" />

### 构造函数和枚举类

枚举类：

- `AnimationType` 

  作用域：`HoverFillButtonBase`、`HoverFillButton`

  ```python
  class AnimationType(Enum):
    CircularFill = 0,  # 进入点圆形填充
    CrossFill = 1,  # 左右两个小圆交叉填充
    DiagonalRectangle = 2,  # 斜着的矩形填充
    BottomCircle = 3,  # 底部圆形填充
    LeftRectangle = 4  # 左侧矩形填充
  ```

构造函数：

- 同`QPushButton`类，但额外添加参数：`AnimationType`枚举，用于控制动画类型，默认动画类型为`HoverFillButtonBase.AnimationType.CircularFill`
- 在designer中通过拖拽或“提升为”使用时，可以通过`def setAnimationType`设置动画类型

### 成员函数说明

<table>
    <thead>
        <tr>
            <th>成员函数</th>
            <th>功能说明</th>
            <th>参数</th>
            <th>参数说明</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>def addShadow</td>
            <td>为按钮添加阴影效果</td>
            <td>int<br>
                int<br>
                float<br>
                QColor</td>
            <td>阴影右偏移量<br>
                阴影下偏移量<br>
                模糊半径<br>
                阴影颜色</td>
        </tr>
        <tr>
            <td>def setTextColor</td>
            <td>设置按钮文字默认颜色和悬浮时颜色</td>
            <td>QColor</td>
            <td>QColor</td>
            <td>按钮默认文字颜色<br>按钮悬浮时文字颜色</td>
        </tr>
        <tr>
            <td>def refreshRadius</td>
            <td>使用样式表修改按钮的圆角半径后,需调用此函数更新圆角半径</td>
            <td>int</td>
            <td>对应样式表中的圆角半径值</td>
        </tr>
        <tr>
            <td>def setFillSpeed</td>
            <td>控制填充速度</td>
            <td>int</td>
            <td>越小填充越快,最小值为1</td>
        </tr>
        <tr>
            <td>def setFillBrush</td>
            <td>设置填充内容绘制笔刷</td>
            <td>QBrush</td>
            <td>自定义的笔刷样式</td>
        </tr>
        <tr>
            <td>def setAnimationType</td>
            <td>设置动画类型,预提供了5种动画</td>
            <td>HoverFillButtonBase.AnimationType</td>
            <td>动画类型枚举</td>
        </tr>
    </tbody>
</table>


<div align="center">
  <h1>其余控件编写中......</h1>
</div>
