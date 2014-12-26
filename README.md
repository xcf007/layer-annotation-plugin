layer-annotation-plugin
=======================

photoshop layer annotation plugin for web front developer

如今各大语言提供了注解机制，极大的简化了开发人员的配置工作。
然后photoshop切图工作一直在由人机械式的去执行，为什么不能交由机器去完成这项苦逼的工作，缺的其实仅仅是一种规范，通知photoshop如何去做这件事情，其实只要adobe公司在photoshop的新建模版中加入一个多行文本框，用了存储@Annotation注解就行了，剩下的看我如何道来：
1. 图层嵌套对应HTML标记嵌套
默认是div标记嵌套
如果想要使用其他标签，那么：
设置为:
{
  tagName:"span"
}
设置样式:
{
  tagName:"span",
  style:{
      ​float:'left',
      "font-size":"12px",
      color:'#c00'
  },
  styleMode:'inner',
  styleName:['textContainer','sideMenu'],
  text:'测试内容'
}

生成代码=>
<span class="textContainer sideMenu" style="float:left;font-size:'12px';color:'#c00';">测试内容</span>

2.默认没有注解的图层将不会产生代码
3.图层文件夹上可以设置内图层是否合并图层结果


