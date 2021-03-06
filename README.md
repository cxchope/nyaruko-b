# wpNyaruko-W 1.3

- 雅诗的个人网站中使用的 WordPress 主题 wpNyaruko-W 。
  - 分支于由 kagurazakayashi(神楽坂雅詩) 和 0wew0 共同开发的「wpNyaruko」主题。
  - W 分支为雅诗个人维护的分支，拥有更多的自定义选项和可扩展功能。更新比源分支新，新增的功能成熟后会反馈回源分支。
  - 此分支虽然提供了很多自定义设置，但仍然主要是以自己个人网站为目标开发的，因此不保证在其他网站上可以正确运行。
- 这是[雅诗个人网站项目](https://github.com/kagurazakayashi/kagurazakayashi.github.com)的一部分。
  - 这是雅诗制作的第一个 WordPress 主题。（自己的网站终于是自己手打的代码啦，也借此学会了怎么做主题~）

## 功能

主题具有 响应式布局，动态加载文章，随机主题元素，特殊页面 等功能。所有的个性化选项功能只在此 W 版本中提供。

- 大头图布局。
- 菜单栏和底部版权栏为相对半伸出布局。
- 顶端图片和底端图片分别显示主题图片的上半部分和下半部分。
- 主题图片为随机图片，从文件夹中抽取，每次刷新随机一张，可在主题设置中修改源。
- 右上角提供随机文字，从数据库中抽取，点击出处名称可前往萌百查词条，可在主题设置中修改源。
- 随机文字中的出处词可以点击在搜索引擎中查询，可在主题设置中自定义搜索引擎。
- 多处元素有轻微的鼠标移过效果。
- 响应式布局，菜单和底栏可变为全宽或最小化到右下角可展开菜单，并可在主题设置中修改响应阈值。
- 主菜单可以进行翻页，主菜单项采用分散对齐。
- 文章列表为固定尺寸块状布局，平铺于屏幕。
- 鼠标移过文章列表时有阴影和图片的动画效果。
- 改变窗口大小时有块重新布局动画。
- 点击前往文章页时有展开平滑过渡网页的动画。
- 动态加载，网页到底部时自动加载更多文章到列表中。
- 可以创建特殊页面，可以实现在页面中写链接自动跳转和写 JSON 自定列表。
- 自定义的鼠标指针。
- 简洁的搜索框。
- 文章页小工具区域根据响应式布局自动移动。
- 可以小窗显示的隐私策略等通知内容。
- 可以从分类目录、搜索、JSON 文章来创建列表。
- 提供主题设定页面。
- 自由更改多处颜色设置。
- 可以统一更改文章格式，字体、字号、首行缩进、行距 等。
- 可以在每个文章/页面前面加入文章作者介绍，显示每个作者的简介，文章/页面可单独启用。
- 可以在每个文章内容顶部显示自定义的原创版权提示或转载来源信息，防止版权问题。
- 提供自定义页头功能，可供加载额外的 css 和 js 文件以及 meta 描述。
- 提供自定义页脚功能，可供填写版权信息，备案号，以及统计代码。
- 提供首页顶部左侧模块自定义。可以设置为短代码，方便配合其他插件（如滚动图）使用。
- 可以设定预览保留字数和查看全文提示语。
- 使用了 svg 矢量图形，并且可以从设置中改回使用 png 。
- 可以在指定位置显示当前网页二维码。
- 评论可以指定为第三方评论系统而不加载本地评论，并可在载入前显示自定义信息。
- 评论输入邮箱后会实时显示头像。
- 可以让 Gravatar 头像走服务器转发或自定义代理，加速用户访问。
- 随时管控 RSS 订阅。
- 评论头像右下角显示该评论发布时用的系统环境图标，鼠标移过显示浏览器和系统版本信息。
- 点击评论处自己的头像可以打开的 gravatar 资料以变更头像等。
- 点击别人的头像可以打开那个人的网站。
- 按回车可以直接发表评论。
- 可以在设定中随时开启和关闭调试模式（显示PHP错误信息输出）。
- 可以自定义访问博客时在控制台输出的欢迎语。
- 可以检查浏览器是否兼容，如果不兼容可以跳转到指定页面，也可关闭兼容性检查。
- 控制台输出的欢迎语可以附带输出页面的处理时长。
- 以及很多来自友链页「YashiLink」中的效果。

## 自定义功能

### 菜单翻页

主菜单一般只能容纳5项（每项2-3汉字），可以使用翻页功能以显示多达8项内容（包含前后翻页项的情况下）。

1. 在 WP 后台中的 `外观` - `菜单` 里分别制作 主菜单第一页 和 主菜单第二页。
2. 转到下一页或上一页的菜单项使用 `自定义链接` 链接到 `#mainmenupage#`。
3. 在管理位置中指派它们。

例子：

- 主菜单第一页：` 首页 新闻 博客 更多>`
- 主菜单第二页：`<返回 相册 友链 关于 `

### 自定义列表

自定义列表项，代替自动生成的文章列表

1. 创建一个页面。
2. 定义每个块显示的内容，包含在`[JSON][JSON]`对中。
3. 为此页面使用「自定义列表」模板。

例子：

`[JSON][["分类","日期","标题","正文","图片","链接"],["type","date","title","txt","img","goto"]][JSON]`

### 自定义静态网页页面

使用自己的网页代替某个页面(例如主页)

1. 创建一个写有目标网址的页面。
2. 网址包含在`[GOTO][GOTO]`对中。
3. 为此页面使用「自定义列表」模板。

例子：

`[GOTO]/home.html[GOTO]`

### 使用自定义代码作为页面内容

将一个 html 文件导入到正文区域，适用于制作互动型页面。

1. 创建一个写有要导入的HTML网址的页面。
2. 如果只导入目标网页中的其中一个div，请加入英文逗号分隔，分隔后面写「.class名」或「#id名」或「元素名」。
3. 网址包含在`[IMP][IMP]`对中。
4. 为此页面使用「导入HTML文章」模板。

例子：

`[IMP]about.html[IMP]`
`[IMP]about.html,body[IMP]`
`[IMP]about.html,#homediv[IMP]`

### 使插件作为首页顶部左侧模块

在主题设置中的「首页顶部左侧模块自定义HTML」中，可以填入 HTML 代码，也可以填入 Wordpress 短代码。

例子：将「Huge-IT Slider」滚动图片插件加入到里面：

1. 在此插件中创建 Slide ，获得这个 Slide 的 Shortcode 。
2. 在主题设置中的「首页顶部左侧模块自定义HTML」中，填入这个 Shortcode（例如 ` [huge_it_slider id="1"]` ）。
3. 勾选「将这些内容理解为 Wordpress 短代码」并保存设定。

### 二维码

要获得当前文章/页面的二维码，使用主题内置小工具「当前页面二维码」即可。

或者，直接插入以下代码到需要的地方：

`<div id="qrview"></div><script type="text/javascript">qr();</script>`

`qr()` 可以输入以下参数：
- text（要编码的文字） = ""（默认值为当前页面网址）
- divid（要填入div的ID） = ""（默认值为"qrview"）
- imgtype（输出格式） = tab（表格）,svg（矢量图）,img（普通图片）（默认值：tab）
- type（类型） = 1-40（默认值：10）
- errorcorrection（容错级别） = L,M,Q,H（默认值：L）
- mode（内容模式） = Numeric,Alphanumeric,Byte,Kanji（默认值：Byte）

小工具和插入代码的参数默认值可以在主题设定中修改。

### 原创与转载提示文本

1. 在主题设定页中的「原创和转载提示」处设定对于原创文章在其内容顶部显示什么提示，以及对于转载文章在其内容顶部显示什么提示。
- 可以在文字中插入 `[URL]` 来显示链接，例子：
  - `这是一篇原创文章，转载请注明来自[URL]。`
  - `本文章转自[URL]，版权归原创者所有。如果侵犯了你的权益，请通知我及时删除。`
2. 在编辑文章画面中，找到「自定义模块」中的「转载自」：
- 对于转载文章，显示转载文章提示文本：
  - 填写来源网站和链接，用英文逗号分隔。
  - 例子：
    - `雅诗的个人网站,http://www.yashi.moe`
- 对于原创文章，显示原创文章提示文本：
  - 留空即可。

## 截图

WP主题显示图：
![WP主题显示图](screenshot.png)

文章列表截图：
![文章列表截图](ScreenShot/screenshot2.jpg)

文章和页面截图：
![文章和页面截图](ScreenShot/screenshot3.jpg)

主题设置：
![主题设置](ScreenShot/screenshot1.jpg)

## 兼容性

- 欢迎使用最新版 Chrome 浏览器，这是该主题的开发环境。
- 支持其他带有最新版 webkit 内核浏览器。
- 可以适配最新版 Firefox 浏览器。
- IE 去死。
- 欢迎使用最新版 iOS 里的 Safari ，这是该主题的开发环境。
- Android 请使用最新版 Chrome 浏览器。
- WP IE 去死。
- 要正常使用，浏览器必须开启 JavaScript 。
- 要保存个性化设置，浏览器需要开启 Cookie 。

## 使用的第三方软件

- [jquery](https://github.com/jquery) / [jQuery](https://github.com/jquery/jquery)
- [kazuhikoarase](https://github.com/kazuhikoarase) / [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator/tree/master/js)

## 许可协议
- wpNyaruko-W（本仓库）
  - MIT License.
- wpNyaruko
  - 定制服务，商业授权。

```
                   ,;;77;
                 ...     7
            .;;;,       7D
          .7;.          S
         ::           ;3;.,.
       ..        ..;:;T;,;;;;, :.
      :.       ,,,77TJ:,::;:;: .,,.               .
     :        JY.;;Y;;:::;;;.  ..:;.             ..
    :        Jh;.:J;.,7:;;:   ..:,;;            ...
   :.       .3J7,7;.,:;;.:,::;..;;:;:           ::
  .,        cT;;JY;.:;:7,;7:;;;.;;:;;         ..:;...
  :        .C;7vU17.:7;Y:777;:7,:7::;.     ..:..:. ..,.
  .       . YJU77;Y,7c7;Y:..c;Y:;J;.;.    : .:,.:..   7::
            xhTT7C97v7,.TTGZv7v:YJ7;;;       ..;:::. .7; ;
,          .7xuH7 @7.   .7@@c;,;E77777;      .:,,.,;7;v, ,
:            :H1T  .      7: ..;7Tc7777v777Ic,:: 7;, ;7 .:
;             EYh           ,.7vGhh3c7;;;;7;..: ,;.,TT;.,
,            T7:CT.  ;;;   ::I@@R37UC3c77v: .,  ;::7;.:
:           :J .UUT;;  .  uH;@b    .7I1SS. .,. 7T77;.
;          .7  7IY ;@@BH:@B.@R   .:T.  .. ... :CJcJc7;:::.
.     .   .;.  v;.  @@BJYR Y@c .:.Z;  . .... .T7vcITTcc;;;7
          ;        :Z;;T;,:@Bu..;;JY      ...Tv;,  .;YUI7;;c
  IYYcvc;::  .;;. ;H,:TT:.J3@B, :. ;.:7;77YYIvJv7;.   ,.:;;;.
 .b  .,:v;:;::GE7cZuc;bR.7 ;b@U  :. ,YcYJJTJ;cYcJYcv.     77.
 :Y    ;.     ;  777;1@;:Y77u@b  : ;bHG7;;;;  .7TJ77Y;. .  c:
  .   ;c      ;: 37:@@b.ZSx7;@@D.  YY  ,.,,;7;  .777;77;   7;
     .;;       7 ;, ;cx,@YJ ;;CB@H.;Zv7IHUGZ;77    ;7;777  ;;
     ;..;      ,;      ;RT.,c.ZG6B6bB@@@bB@GU777    ;Y;77: ;
     ;: v;.     .:,   :: G1U@@BEb7x@6h0b9GDC, :;7    ;;,cc;
      ;  ..       .:,,;; ;@@bbb@bB1YDDHbRBB6T  ;v;    ; ;;7
      .,             E@.b@B6R9b@Y7;,uRE6bBBb@@@REbh  .. ; 7.
                   :;@@,;@b99Rb@;  .:@60bb;   .  T@3    7 7.
                ... 0;bT Yb696@RU;..ERGubb7c      S7   ;, :
             .,,     7BB;7669b;  ;T;UR3SR@.TTb    ;.   .
            ,.       .;Y@3Bb9DUvhB@CG096@J ;U7   ..
           .        .  7J.@bRbBBbR@@@Rb@ 7:YU@
         .:     ..;;;;;:;vI;@HBBBDb@xR@.:U 6;T
        :;,..:;;;;:::...   .E;u07@S7TC,;B.76
        .;;;;;;.  .        3@    x7 RI YR
           .               G:      :
                                  .;  .
                                  .;...
                                   ;; .
                                   ;:.
                                   ;:.
                                  ::
                                 ;;;
                                ;;;;
                              ,;:7:
                              RS7
```