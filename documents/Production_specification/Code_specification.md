# 代码规范
| 版本 | 日期 | 描述 | 作者 |
| - | - | - | - |
| v1.2 | 2019.4.24 | 代码规范 | LYM |
## 目录规范
### 图片文件
所有项目图片统一放在根目录的images文件夹下相应的子文件夹内。
### 代码文件
同一页面的wxml、wxss、js、json文件放在同一文件夹内，所有页面文件统一放在根目录的pages文件夹内
## WXML规范
1、代码长度

  控制每行HTML代码数量在80个字符内，以便于阅读，多余代码进行换行处理。

2、缩进

  保证同一组标签的缩进相同，且尽量使得独立的标签占据单独的一行。
  
3、注释

  文件首行添加该文件的路径注释，在需要注释的标签上一行进行注释，代码块之间空行来划分结构块。
  
4、id/class命名
  
  优先根据内容进行命名，采用驼峰命名法，即首个单词使用小写，之后的单词首字母大写，其余小写，例如buttonList、submitButton、lostTitle。
~~~
<view class="contain">
  <button  open-type="getUserInfo" bindgetuserinfo="getUserInfo" type='primary'> 微信授权登录 </button>
</view>
~~~
## WXSS规范
1、注释
  
  文件首行添加该文件的路径注释，在意义不明确的样式名上一行添加注释。
~~~
/*感谢语*/
.peroration{
  font-size: 15pt;
  margin: 20rpx 20rpx;    
  color: rgb(13, 141, 245);
}
~~~
2、代码缩进

每个样式内的属性前缩进一个TAB。
## JS规范
JavaScript规范使用[ES2016+](http://kangax.github.io/compat-table/es2016plus/)
## 标点规范
* JS语句统一省略分号。
* JS中统一使用单引号''，WXML、CSS、JSON中均使用双引号""。
* 所有文件中，冒号后用一个空格分隔。
* 执行一致的缩进（1个TAB）。
