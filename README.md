![](https://github.com/loperSeven/DateTimePicker/blob/master/images/title.png)
<br/>
[![](https://jitpack.io/v/loperSeven/DateTimePicker.svg)](https://jitpack.io/#loperSeven/DateTimePicker)&ensp;[![API](https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=21)&ensp;[![](https://img.shields.io/badge/platform-android-green)](https://github.com/loperSeven)&ensp;[![](https://img.shields.io/badge/license-MIT-blue)](https://opensource.org/licenses/MIT)
<br/>
## Language
中文 | [English](https://github.com/loperSeven/DateTimePicker/blob/master/README_EN.md)
<br/>
<br/>
DateTimePicker 一个简约、漂亮的日期时间选择器，支持大面积自定义UI，内置日期时间选择弹窗，基于 Google BottomSheetDialog，可直接使用。
<br/>
## 预览
加载不出图片可以前往 [简书](https://www.jianshu.com/p/5610db432512) 或 [掘金](https://juejin.im/post/5ecf7699e51d4578644e9320) 查看
<br/>
![](https://github.com/loperSeven/DateTimePicker/blob/master/images/gif.gif)![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_1.jpg)![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_2.jpg)
![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_3.jpg)![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_4.jpg)![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_5.jpg)
![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_6.jpg)![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_7.jpg)![](https://github.com/loperSeven/DateTimePicker/blob/master/images/image_8.jpg)
<br/>
## 快速体验
![](https://github.com/loperSeven/DateTimePicker/blob/master/images/app_qrcode.png)
<br/>
或者&ensp;[点击下载](http://fir.cqtencent.cn/dtpicker)
<br/>
## 如何引入
Step 1. 添加 JitPack repository 
```
allprojects {
	repositories {
		...
		maven { url "https://jitpack.io" }
	}
}
```
Step 2. 添加 Gradle依赖
```
dependencies {
    ...
    implementation 'com.google.android.material:material:1.1.0' //为了防止不必要的依赖冲突，0.0.3开始需要自行依赖google material库
    implementation 'com.github.loperSeven:DateTimePicker:$version'//具体版本请看顶部jitpack标识，如0.2.2,仅支持androidx
}


```
## 如何使用
日期时间选择控件
<br/>
&ensp;&ensp;[DateTimePicker 使用说明](https://github.com/loperSeven/DateTimePicker/wiki/DateTimePicker-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E)
<br/>
卡片弹窗
<br/>
&ensp;&ensp;[CardDatePickerDialog 使用说明](https://github.com/loperSeven/DateTimePicker/wiki/CardDatePickerDialog-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E)
<br/>
## 更新日志
### [v0.2.2](https://github.com/loperSeven/DateTimePicker/releases/tag/0.2.2) -> [v0.2.3](https://github.com/loperSeven/DateTimePicker/releases/tag/0.2.3)
* fix [issues 11](https://github.com/loperSeven/DateTimePicker/issues/11)

### [v0.2.1](https://github.com/loperSeven/DateTimePicker/releases/tag/0.2.1) -> [v0.2.2](https://github.com/loperSeven/DateTimePicker/releases/tag/0.2.2)
* fix [issues 10](https://github.com/loperSeven/DateTimePicker/issues/10)

### [v0.2.0](https://github.com/loperSeven/DateTimePicker/releases/tag/0.2.0) -> [v0.2.1](https://github.com/loperSeven/DateTimePicker/releases/tag/0.2.1)
* fix [issues 7](https://github.com/loperSeven/DateTimePicker/issues/7)

### [v0.1.1](https://github.com/loperSeven/DateTimePicker/releases/tag/0.1.1) -> [v0.2.0](https://github.com/loperSeven/DateTimePicker/releases/tag/0.2.0)
* 新增DateTimeController逻辑控制器，以支持UI 100% 自定义
* 重构DateTimePicker，抽离逻辑至DateTimeController,自身仅控制UI
* 抽离常量至DateTimeConfig
* 抽离像素单位转换至ContextExt拓展
* fix [issues 4](https://github.com/loperSeven/DateTimePicker/issues/4)-CardDatePickerDialog.Builder内变量添加@JvmField以支持Java调用

### [v0.1.0](https://github.com/loperSeven/DateTimePicker/releases/tag/0.1.0) -> [v0.1.1](https://github.com/loperSeven/DateTimePicker/releases/tag/0.1.1)
* 修复设置最大年份后，当选择到最大年份时，月份为0的问题
* 修复范围最大值，范围最小值，选中默认值之间冲突时约束异常问题（规则为：最大范围值与最小范围值存在冲突时，后设置的值不会生效；选中默认值与范围最大值/范围最小值存在冲突时，不会生效）
* 优化监听回调代码，使用kotlin特性，使回调更加简洁
<br/><br/>eg:感谢 [yaolv7](https://github.com/yaolv7) 提供的Pull requests
### [v0.0.7](https://github.com/loperSeven/DateTimePicker/releases/tag/0.0.7) -> [v0.1.0](https://github.com/loperSeven/DateTimePicker/releases/tag/0.1.0)
* DateTimePicker类变更为kotlin编写
* 新增单位标签可在代码内配置
* 移除DateTimePicker回调监听非必要字段
* 新增CardDatePickerDialog取消、确定按钮文字配置
* 新增CardDatePickerDialog取消按钮回调监听
* 变更CardDatePickerDialog监听绑定至builder内
<br/><br/>eg:此次更新对原有方法及配置有一定改动，详情查看 <strong>[ 如何使用 ]</strong>

## 混淆
```
-dontwarn com.loper7.date_time_picker.**
-keep class com.loper7.date_time_picker.**{*;}
```
## 感谢
[Number Picker](https://github.com/ShawnLin013/NumberPicker)
<br/>
## 联系我
Issues：[Issues](https://github.com/loperSeven/DateTimePicker/issues)
<br/>
邮箱：loper7@163.com
<br/>
## Licenses
```
Copyright 2020 loperSeven

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

