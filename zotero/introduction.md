# 文献管理软件Zotero入门

## 写在前面

　　依旧先向[阳志平](http://www.yangzhiping.com/)老师的[Zotero系列教程](http://www.yangzhiping.com/tech/zotero1.html)致敬。前一段在群里聊，突然有想再写一篇Zotero入门教程的想法，不过想想阳老师的的入门教程，除了设置软链接略显的过时，其余内容实在全面且精彩，于是感觉自己写一篇非常的鸡肋。不过终究动笔了，希望这是一篇有所不同的入门教程，它可能不太客观，对新手也不够亲和，但会让更多人有所收获。读完这篇教程，你有可能还是不会用Zotero，但是你会对现在的主流的文献管理软件有个大概的认识，它可能会成为你学习Zotero的动力。

　　文章原载于本人的项目，我自行搬运到简书上为大家阅读方便，欢迎有货之士为我的文献管理项目添砖加瓦！

## 冗长文献管理历史(可跳)

　　几乎所有人，使用文献管理软件的原动力，可能都是为文章加入参考文献，因为这项工作一点一点敲字母会非常繁琐。有人会告诉我说Google学术可以复制参考文献，也不算很麻烦。所以我把直接Google学术复制文献信息的问题列一下：

1. 有人上不去Google学术，不过这样Zotero也用不舒服，但姑且算一点。
2. 文献信息有错，而且并不少见。
3. 输出的格式有限，并不能完全满足不容的需求。
4. 即使交叉引用，也很难修改引文序号 (交叉引用：Word中一个实现自动排号的功能)。

　　因此，对一名相对严谨的科研狗来说，Google复制并非上策。于是我们投身于各种文献管理软件，以CSL的出现和使用为界，我将文献管理软件分为两代，上一代是大家耳熟能详的EndNote和国产软件NoteExpress，这一代的就是以Zotero，Mendeley，Docear为代表的基于CSL的文献管理软件们。

　　当然CSL(Citation Style Language的缩写)的出现，仅有标志性的意义，两代文献管理软件风格和设计理念的差异才造成这样划分的根本原因。在Elsevier强推Mendeley之前，几乎用文献管理软件的人，都会至少用过EndNote和NoteExpress其中的一个，那时候EndNote就是文献管理软件的模板，这些多少含有数据库背景的商业软件，设计的思路是从数据库的维护者的角度出发的，软件功能极其**复杂**，对用户并不亲和，换句直观的话就是，**功能很多，但并没有什么卵用**。

　　相对前一代**数据库背景**的**闭源商业**文献管理软件，新一代管理软件从用户角度出发，**免费**，很多**开源**，对用户**亲和**。那么，新一代文献管理软件是怎么亲和的，而为什么我对Zotero情有独钟呢？请看下回分解，哦不，下一部分。

## Zotero的特点

　　文献管理软件最重要的两部分功能，一个是文献的收录，另一个就是在文字编辑器里面插入，要求再多一些还有文献数据库的组织。

### 文献收录

　　根据我的理解，文献的*主要*收录途径有3大类：
> 我任性的去掉了其他软件/数据库文件导入，手动输入，基于以下原因：开源软件并不强势，其他软件的导入是必须的，但也必然伴随折腾或者不完美，最主要的是，我忘了怎么弄了，因为很少有人天天换文献管理软件玩；数据库导入，支持，在爬虫面前显得鸡肋，后面再解释；手动输入，支持，不过你确定你要一直这么干？
> 写到这里，我默默的看了一眼Zotero的import功能，打开文件支持的类型，有一长串，这都是什么鬼！我也明白阳志平老师为啥连他大纲里面的导入功能都没写完了，因为，他也觉得越写越多...

1. 网络爬虫爬网页信息
2. 通过数据库的api
3. 读取pdf元数据

　　然而这三点，分别对应了Zotero的三个*主要*录入功能：浏览器插件的translator功能，主界面小魔棒标示符，右键菜单从pdf读取元数据。

#### 浏览器插件

　　浏览器插件的translator功能是在网页上爬文献的元数据，这几乎是Zotero最耀眼的功能，Zotero前身只是一个安静的火狐插件，后来才成为独立软件，在它之后，NoteExpress做了浏览器插件，还出现了纯基于网络的RefME，但是这些软件在功能上，都比Zotero上有所欠缺。
　　
　　聊浏览器插件，按照Zotero的思路，从不同的文献的类型来看：

1. 期刊：这个是最常见的类型，支持非常多的全文数据库、文摘数据库，大概有点名字的都没问题，国内支持万方和知网[cnki.net](http://www.cnki.net)域名。
> 彩蛋1: 知网下不到PDF？请访问: [CNKI PDF 全文下载用户脚本](http://blog.yuelong.info/post/cnki-pdf-js.html)
> 彩蛋2: 中文的数据库题目和作者都是中文不够International？请访问[知网英文版](http://oversea.cnki.net)

2. 书籍：豆瓣和亚马逊，各种亚马逊，中亚，美亚，你能想到的各种亚...

3. 专利：支持[Google专利老域名](www.google.com/patents)，不支持[Google专利新域名](patents.google.com)。
> 彩蛋3: 专利又不够International?请在你访问的网址最后加上 \&cl=en，这是改内容的语言，网页的语言的修改是 \&hl=en，如果你搜个汉语名字，出来发明者的名字也是汉语的我帮不了你，你得自己改成对应的英文。

4. 学位论文: 基本都支持，这方面我不太懂，有懂的同学可以编辑一段我加进来。

5. 其他: 维基百科，Github，Youtube，都支持，别问我为什么知道的。

　　常用的大概也就这些了，稍微有点遗憾的是标准不支持，但是和CSL有关系，详细的后面谈。

　　那么刚刚在数据库文件导出哪里我说，数据库导出功能不如直接用translator，因为在文摘数据库里，有个文件夹状态的translator，用这个文件夹translator可以导入多篇文献，而且灵活简单，完爆数据库导出再导入Zotero.

#### 标示符导入

　　标示符相当于一篇文章/一本书的二维码，和文章/数据具有一一对应关系。标示符有三种DOI，ISBN，PMID，他们分别对应着：

* DOI: 多数的外文期刊，少数的外文数字书籍
* ISBN: 所有的书籍
* PMID: pubmed搜索引擎中的文献

　　由于PMID使用偏医药方向，我从来没用过，DOI和ISBN还是比较常用的。对于书籍我一般先试ISBN再去用浏览器插件，而文献的顺序恰好相反。

　　这三种标示符的导入，都需要数据库公开API的支持，这也就导致了为何知网万方的文献都有DOI但是依旧无法通过DOI导入数据。说到这里我还有些困惑，中国的期刊DOI到底算不算DOI，因为DOI是一篇文献只有一个，加DOI是杂志社的行为。但是在中国，却是数据库的行为，很多文献，知网和万方都有，也就是一篇文献有两个DOI，我觉得知网和万方的DOI只能算伪DOI，他们仅仅有个重定向的功能，仅此而已。

#### 从PDF读取元数据

　　这可能是新手最向往的功能，但是我几乎没用过，而且我不推荐用这个获取文献信息，下面我解释它的作用原理和局限。

　　从PDF读取元数据，那么元数据在哪里？不要太天真的想象这个读取元数据，类似爬虫一样去文章的全文中爬出作者，题目期刊之类的信息，最起码现在还不是这样的。PDF元数据就写在文章的属性里面，windows下右键属性就能看到。你可以看到英文年代不太久远的，几乎都有，但是对于中文期刊不是乱码就是空的，为什么？因为生成pdf的方式不同，近年来的国外期刊，都是利用$\LaTeX$进行的排版，作者题目期刊等信息自动写到PDF的属性里去。否则为何提交个文章要把作者写那么清楚，正文里不都有吗？然而中文的期刊，现在几乎都还停留在Word为主的提交方式，这并不low但是，它转成的PDF如果再想加入作者信息，会比较麻烦。

　　这导致，从PDF获取文献信息，尤其是中文文献信息的极大局限性。
> 谈到中文文献，我不得不再说两句，DOI不好用，元数据没有，可以说对中文支持最好的**开源**软件一定是Zotero，因为它的获取文献的机制还有一个浏览器插件。反过来说，如果你确实中文献需求量很大，那么知网的E-Study是你最好的选择，因为它获取文献的方法应该是内部的API，非开源软件能及。

　　与此同时，PDF元数据里的东西，也不一定完全正确，但是Zotero在此的努力暂时就到此了。不过，还有另外的两个软件再这个功能上走的更远：Endnote和Mendeley。

　　Endnote的展开就此一段，不吹不黑。Endnote导入文献最舒服的方式是用自带引擎搜索，其次是DOI(可能没有直接功能，可以通过新建空白文档，填入DOI)，读取元数据好像是自动的，但是不准怎么办？亮点来了: `update with DOI`。使得EndNote可以通过DOI读取的数据对当前数据进行更新，并且可以选择你更新的部分，可谓非常强大。即使元数据不怎么准，那么再来一次DOI也就八九不离十了。

　　Mendeley我对它并没有什么偏见，如果满分10分的话，没装插件的Zotero我能给8分，Mendeley我可以给6分(不过放心吧，EndNote一流，我只会给的更少)，但是嗝应人的是Elsevier的强推。各种讲座使劲的推，作者指导里默默的推，我知道现在是也把Zotero写上了，问题对于新人，他会用推荐软件里的第一个还是第二个？现在群里进来的新人几乎都是踩着作者指导里的Mendenely的坑进来的，并不是说Meneley有多不好，但是和Zotero相比，它只能慨叹一句“既生瑜，何生亮”。

　　Mendeley的主要功能和Zotero相差无几，自定义程度略低，没有浏览器导入功能，优点是，整个数据库的全文搜索**非常快**。它获取PDF元数据也是自动的，因为这个是它获取文献信息的最主要方式，在获取完元数据后，它会自动联网匹配，可以通过文献信息模糊匹配，也可以通过Arxiv ID/DOI/PMID精确匹配，在PDF元数据的基础上，对文献信息进行一次更正。

#### 正在开发

#### 有待提升

* Item Type:标准

* 国标7714支持

* 文件链接的加强

　　也可以说是Zotfile整合的加强，现在删除文献，相应的文献链接不会删除，在我看来Zotero应该可以胜任这项工作。

#### 未来的路

　　科技发展的速度，给人类生活带来了翻天覆地的变化，地图、支付宝、美团，改变了人们生活的根本方式。未来云端存储及软件会逐渐成为主流，从ChromeBook中可以看到这样的趋势。从刚刚起步的MicroSoft的云端套件，到已经很强大的Google的云端套件，人们能感觉到这一天并不太远。高速通讯网络的普及和城市Wifi的大面积覆盖，让以云端为主的工作方式，提供了云端办公的坚实支持。未来的文献管理也是如此，我预言，得云端者得天下！

* 社区化

* 云端文字编辑器支持

* 快照的美化编辑及存储