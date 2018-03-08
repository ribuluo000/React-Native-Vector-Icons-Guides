# React-Native-Vector-Icons-Guides

文章地址: [React Native与Iconfont](https://github.com/MrErHu/blog/issues/15)

运行:

1. `npm install`

2. iOS: `react-native run-ios`　　Android: `react-native run-android`

# 添加自定义字体注意事项

参考：[React-Native使用自定义字体文件iconfont_https://www.jianshu.com/p/96d5c66791c3](https://www.jianshu.com/p/96d5c66791c3)

- 在project/assets/font目录下放置相关Iconfont的 ****.ttf 文件，将/project/component/Iconfont目录以及目录内的文件复制到自己的项目中对应的位置。
- 按参考的链接，将想要用的 ****.ttf 文件，添加到IOS和Android项目中。
- 在/project/component/Iconfont/Iconfont.json 文件中添加对应的“name”:number值(
如果 ****.ttf 文件在阿里巴巴矢量图库中得到，则会生成 ****.ttf 文件的同时，会生成 demo_unicode.html ,里面内容类似：

```
                <i class="icon iconfont">&#xe625;</i>
                    <div class="name">arrow-down</div>
                    <div class="code">&amp;#xe625;</div>
                </li>
```

则需要手动将name和number对应起来，尤其是number要注意，以上面的例子为例：
name:number ,
可以写为
"arrow-down":58917,

其中 58917为 十六进制code e625的十进制对应的数字。

在线进制转换
[http://tool.oschina.net/hexconvert](http://tool.oschina.net/hexconvert)

![](https://raw.githubusercontent.com/ribuluo000/React-Native-Vector-Icons-Guides/master/%E5%9C%A8%E7%BA%BF%E8%BF%9B%E5%88%B6%E8%BD%AC%E6%8D%A2.png)


)

- eg:{
  "Github": 59189
}

- 使用

eg:

```
import Iconfont from './component/Iconfont'


<Iconfont name="Github" size={30} color="#8a8c8e"/>


```






