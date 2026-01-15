---
title: "数据结构-图论"
summary: "数据结构图论章节的一些总结"
tags: ["数据结构","图论",]
categories: ["数据结构与算法"]
#externalUrl: ""
#showSummary: true
date: 2022-03-18
draft: false
---

<span style=";font-family:宋体;font-size:14px">这是我的结课总结，认识或许还有很多不足（自己也能感觉到自己的菜），仅供参考，请勿抄袭，谢绝转载，谢谢！ </span>

<span style=";font-family:宋体;font-size:14px">如有不懂，可发友善留言讨论。</span>

<span style=";font-family:宋体;font-size:14px">目录</span>

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">一、</span> </span><span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">图的定义极其相关基本概念</span></span> ](#_Toc17825)

[<span style=";font-family:黑体;font-size:14px">1.1 </span><span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">图的定义</span></span> ](#_Toc11785)

[<span style=";font-family:黑体;font-size:14px">1.2 </span><span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">图的相关概念</span></span> ](#_Toc32436)

[<span style=";font-family:黑体;font-size:14px">1.3 </span><span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">图的抽象数据类型</span></span> ](#_Toc32507)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">二、</span> 图的存储</span> ](#_Toc14211)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">2.1 图的邻接矩阵存储</span></span> ](#_Toc28996)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">2.1.1 无向图的邻接矩阵表示</span></span> ](#_Toc11174)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">2.1.2 有向图的邻接矩阵表示</span></span> ](#_Toc20606)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">2.1.3 函数解析</span></span> ](#_Toc1323)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">2.2 图的邻接表存储</span></span> ](#_Toc24562)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">2.2.1 无向图的邻接表表示</span></span> ](#_Toc32226)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">2.2.2 有向图的邻接表表示</span></span> ](#_Toc3892)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">2.2.3函数解析</span></span> ](#_Toc30729)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">2.3 图的度</span></span> ](#_Toc3228)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">2.3.2 邻接表求度数</span></span> ](#_Toc12642)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">2.4 两种存储方式的比较</span></span> ](#_Toc27778)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">2.5 带权图</span></span> ](#_Toc17569)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">三、</span> 图的遍历</span> ](#_Toc16146)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">3.1 广度优先遍历</span></span> ](#_Toc24131)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">3.1.1 算法分析与方法选择</span></span> ](#_Toc29208)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">广度优先遍历过程图示图示</span></span> ](#_Toc19344)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">3.2 深度优先遍历</span></span> ](#_Toc1204)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">3.2.1 算法分析与方法选择</span></span> ](#_Toc15185)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">3.2.2 递归法</span></span> ](#_Toc6478)

[<span style=";font-family:宋体;font-size:14px"><span style="font-family:宋体">3.2.3 非递归法（栈法）</span></span> ](#_Toc16905)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">四、</span> 拓扑排序</span> ](#_Toc26416)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">4.1 算法分析</span></span> ](#_Toc9064)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">4.2 应用</span></span> ](#_Toc3756)

[<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">五、</span> 最小生成树</span> ](#_Toc17484)

<span style=";font-family:黑体;font-size:14px"></span>

<span style=";font-family:黑体;font-size:14px"> </span>

<a name="_Toc17825"></a><span style="font-family: 黑体;font-size: 19px">一、</span><span style="font-family: 黑体;font-size: 19px">图的定义极其相关基本概念</span>

<a name="_Toc11785"></a><span style="font-family: 黑体;font-size: 16px">1.1 </span><span style="font-family: 黑体;font-size: 16px">图的定义</span>

<span style="font-family: 宋体;font-size: 16px">图是表示物件与物件之间关系的数学对象。</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<a name="_Toc32436"></a><span style="font-family: 黑体;font-size: 16px">1.2 </span><span style="font-family: 黑体;font-size: 16px">图的相关概念</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">表示方法：二元组或三元组。其中二元组常用，即用</span>“顶点”集合和“边”集合表示。</span>

<span style="font-family: 宋体;font-size: 16px">图的分类：有向图和无向图。</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">度：与顶点</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">相关联的边的条数。对于无向图，可分为入度和出度，以顶点</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">为起点的边的条数即为</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">的出度，以顶点</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">为终点的边的条数即为</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">的入度。</span></span>

<span style="font-family: 宋体;font-size: 16px">图的存储：常用的有邻接矩阵存储、邻接表存储。</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">图的遍历：深度优先遍历（</span><span style="font-family:Calibri">DFS</span><span style="font-family:宋体">）和广度优先遍历（</span><span style="font-family:Calibri">BFS</span><span style="font-family:宋体">）。</span></span>

<span style="font-family: 宋体;font-size: 16px">重要概念：最小生成树，拓扑排序。</span>

<span style="font-family: 黑体;font-size: 16px"> </span>

<a name="_Toc32507"></a><span style="font-family: 黑体;font-size: 16px">1.3 </span><span style="font-family: 黑体;font-size: 16px">图的抽象数据类型</span>

<span style="font-family: 黑体;font-size: 16px">ADT</span><span style="font-family: 宋体;font-size: 16px"> <span style="font-family:宋体">Graph </span></span><span style="font-family: 黑体;font-size: 16px">is</span>

<span style="font-family: 黑体;font-size: 16px">operations</span>

<span style="font-family: 宋体;font-size: 14px">创建一个空图</span>

<span style="font-family: 宋体;font-size: 14px">Graph createGraph(void)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">判断图</span>g是否为空，是则返回1，否则返回0</span>

<span style="font-family: 宋体;font-size: 14px">Int isNullGraph(Graph g)</span>

<span style="font-family: 宋体;font-size: 14px">找图中的第一个顶点</span>

<span style="font-family: 宋体;font-size: 14px">Vertex firstVertex(Graph g)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">找图中顶点</span>vi的下一个顶点Vertex nextVertex(Graph g,Vertex vi)</span>

<span style="font-family: 宋体;font-size: 14px">在图中查找顶点</span>

<span style="font-family: 宋体;font-size: 14px">Vertex searchVertex(Graph g,Vertex vi)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">在图</span>g中增加一个顶点</span>

<span style="font-family: 宋体;font-size: 14px">Graph addVertex(Graph g,Vertex vi)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">在图</span>g中删除一个顶点和与该点相关联的所有边</span>

<span style="font-family: 宋体;font-size: 14px">Graph deleteVertex(Graph g,Vertex v)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">在图</span>g中删除一条边e(<vi,vj>或者(vi,vj))</span>

<span style="font-family: 宋体;font-size: 14px">Graph deleteEdge(Graph g,Vertex vi,Vertex vj)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">在图</span>g中增加一条边<vi,vj>或者(vi,vj)</span>

<span style="font-family: 宋体;font-size: 14px">Graph addEdge(Graph g,Vertex vi,Vertex vj)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">判断图</span>g中是否存在一条指定边<vi,vj>或者(vi,vj)</span>

<span style="font-family: 宋体;font-size: 14px">int findEdge(Graph g,Vertex vi,Vertex vj)</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">找图</span>g中与顶点v相邻的第一个顶点</span>

<span style="font-family: 宋体;font-size: 14px">Vertex firstAdjacent(Graph g,Vertex v)</span>

<span style="font-family: 宋体;font-size: 14px">/*v与返回顶点构成的边也称为与v相关联的第一条边*/</span>

<span style="font-family: 宋体;font-size: 14px"><span style="font-family:宋体">找图</span>g中与顶点vi相邻的，相对相邻顶点vj的，下一个相邻顶点</span>

<span style="font-family: 宋体;font-size: 14px">Vertex nextAdjacent(Graph g,Vertex vi,Vertex vj)</span>

<span style="font-family: 宋体;font-size: 14px">/*vi与返回顶点构成的边也称为是vi与vj构成的边的下一条边*/</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<a name="_Toc14211"></a><span style="font-family: 黑体;font-size: 19px">二、</span><span style="font-family: 黑体;font-size: 19px">图的存储</span>

<a name="_Toc28996"></a><span style="font-family: 黑体;font-size: 16px">2.1 图的邻接矩阵存储</span>

<a name="_Toc11174"></a><span style="font-family: 宋体;font-size: 16px">2.1.1 无向图的邻接矩阵表示</span>

<span style="font-family: 黑体;font-size: 14px">数学表示</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">无向图就是边没有方向的图，对于图</span>G(V,E),V={v1,v2,v3,...,vn}是图G的顶点集，E={e1,e2,e3,...,en}是图G的边集。无向图的每一条边都可以用一个无序对表示，且为圆括号，如e =（vi,vj）表示顶点(vi,vj)之间的边。边(vi,vj)和边(vj,vi)表示同一条边。</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">邻接矩阵是用一个二维矩阵存储图中各个顶点和边的信息的存储方式，它是完全使用顺序存储方式的。在邻接矩阵中，存储的是顶点和顶点之间的相邻关系。对于无权图，用</span>1表示相邻，0表示不相邻。</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">如图所示为一个矩阵（矩阵</span>1），若该矩阵为图G的邻接矩阵（编号从1开始），则矩阵中的a(ij)存储的是顶点v(i)到v(j)之间的边，即边(vi,vj)（或边(vj,vi)）的信息。</span>

<a name="_Toc8755"></a><a name="_Toc12884"></a><a name="_Toc7907"></a>![图片1.png](../img/202203181647605025705046.png)

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">矩阵</span>1</span>

<span style="font-family: 黑体;font-size: 12px"> </span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">对于无向图，由于前文提到的边</span>(vi,vj)和边(vj,vi)是同一条边，故矩阵中a(ij)=a(ji)，从而可以得到如下矩阵（矩阵2）。</span>

<a name="_Toc1621"></a><a name="_Toc28507"></a><a name="_Toc4907"></a>![图片2.png](../img/202203181647605034714736.png "图片2.png")

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">矩阵</span>2</span>

<span style="font-family: 宋体;font-size: 16px">从矩阵中可以看到无向图的邻接矩阵是关于主对角线对称的。</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<span style="font-family: 黑体;font-size: 14px">数据结构表示</span>

<span style="font-family: 宋体;font-size: 16px">前文提到，邻接矩阵的存储是完全地采用顺序存储方式进行存储的。即二维数组实质上是一段连续的存储空间。</span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">typedef</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">struct</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> {</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> vcount;</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> type;</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">char</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> vexs\[N\];</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> arcs\[N\]\[N\];</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} GraphMatrix;</span>

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">代码块</span>1</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">上述代码（代码块</span>1）为邻接矩阵的数据结构C语言代码。其中共有4个成员变量，vcount是记录图中顶点个数的整型变量；type用于指定图的类型，有向图用0表示，无向图用1表示；vex\[N\]是图中顶点的信息；arcs是存储图中边信息的整型二维数组，arcs\[i\]\[j\]表示vex\[i\]和vex\[j\]之间的边。</span>

<a name="_Toc28524"></a><span style="font-family: 宋体;font-size: 16px">2.1.2 有向图的邻接矩阵表示</span>

<span style="font-family: 宋体;font-size: 16px">有向图的邻接矩阵表示和无向图基本相同，仅存在以下几个不同：</span>

<span style="font-family: 宋体;font-size: 16px">（1）</span><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">有向图的</span>“边”称为“弧”；</span>

<span style="font-family: 宋体;font-size: 16px">（2）</span><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">有向图中弧的数学表示方法为有序对，且为尖括号表示，如</span><vi,vj>表示顶点</span> <span style="font-family: 宋体;font-size: 16px">vi到顶点vj的有向弧；</span>

<span style="font-family: 宋体;font-size: 16px">（3）</span><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">如下矩阵，有向图中，邻接矩阵中的</span>a(ij)与a(ji)不一定相等，即其邻接矩阵不一定是对称矩阵。</span>

<a name="_Toc31484"></a><a name="_Toc21751"></a><a name="_Toc23969"></a>![图片3.png](../img/202203181647605052581326.png "图片3.png")

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">矩阵</span>3</span>

<span style="font-family: 黑体;font-size: 12px"> </span>

<span style="font-family: 宋体;font-size: 16px">（4）</span><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">有向图邻接矩阵中的</span>a(ij)表示以vi为起点，vj为终点的边；</span>

<span style="font-family: 宋体;font-size: 16px">（5）</span><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">有向图进行邻接矩阵存储时，仅对于输入的边（</span>vi,vj），仅将二维数组vex</span> <span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">中的</span>arcs\[i\]\[j\]置为1；</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<span style="font-family: 宋体;font-size: 16px">有向图的数据结构和无向图完全一致。</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<a name="_Toc1323"></a><span style="font-family: 宋体;font-size: 16px">2.1.3 函数解析</span>

<span style="font-family: 宋体;font-size: 16px">邻接矩阵的基本操作比较简单，主要有邻接矩阵的初始化、点集的输入和边信息的输入。</span>

<span style="font-family: 宋体;font-size: 16px">(1) </span><span style="font-family: 宋体;font-size: 16px">GraphMatrix \*initGraphMatrix();</span>

<span style="font-family: 宋体;font-size: 16px">函数功能：初始化邻接矩阵，并完成边集的输入（不输入顶点信息）。</span>

<span style="font-family: 宋体;font-size: 16px">输入：图的类型、顶点数、边数；边的起始、终点顶点编号。</span>

<span style="font-family: 宋体;font-size: 16px">返回值：初始化完成并完成顶点集和边集存储的邻接矩阵。</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">主要思路：把图的类型和顶点数、边数输入完成后，首先使用双重循环将邻接矩阵中的每个元素置为</span>0，再输入所有的边，每条边用former表示一端的下标，latter表示另一端的下标。对于无向图（type=0）,将邻接矩阵中的第former行第latter列的元素(arcs\[former\]\[latter\])和第former行第latter列的元素(arcs\[latter\]\[former\])置为1。对于有向图（type=1），则仅将邻接矩阵中的第former行第latter列的元素(arcs\[former\]\[latter\])置为1。</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<a name="_Toc24562"></a><span style="font-family: 黑体;font-size: 16px">2.2 图的邻接表存储</span>

<a name="_Toc32226"></a><span style="font-family: 宋体;font-size: 16px">2.2.1 无向图的邻接表表示</span>

<span style="font-family: 黑体;font-size: 14px">数学表示</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">邻接表是用顺序表和链表混合存储图信息的存储方式，其存储方法与哈希表存储方法中的拉链法类似，即使用一个顺序表保存顶点信息和一个指针域，该指针域指向一个链表，该链表为与该顶点邻接的顶点的链表。邻接表的结构如下图所示</span>,图2是图1所示无向图的邻接表。</span>

![图片4.png](../img/202203181647605084122235.png "图片4.png")<span style="font-family: 宋体;font-size: 16px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">1</span><span style=";font-family:黑体;font-size:13px"> <span style="font-family:黑体">无向图</span></span>

<span style=";font-family:宋体;font-size:14px"> </span>

<span style="position:absolute;z-index:1;left:0px;margin-left:659.7500px;margin-top:260.7500px;width:34.0000px;height:34.0000px">![](http://172.16.157.128/zb_users/plugin/UEditor/themes/default/images/spacer.gif)</span><span style="font-family: 宋体;font-size: 16px">![202203181647605093463291.png](http://172.16.157.128/zb_users/upload/2022/04/202204201650459236816841.png "202203181647605093463291.png") </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">2</span><span style=";font-family:黑体;font-size:13px"> <span style="font-family:黑体">无向图的邻接表</span></span>

<span style=";font-family:宋体;font-size:16px"><span style="font-family:宋体">由图可以看到，在邻接表中，大体上可以分为两个部分，即左边的顺序表和右边的链表，左边的顺序表用于存储顶点以及顶点的信息；右边的链表用于存储图中边的信息，称为边表。每一个顶点都带有一个边表。与某顶点</span><span style="font-family:Calibri">v</span><span style="font-family:宋体">邻接的所有顶点都存储在</span><span style="font-family:Calibri">v</span><span style="font-family:宋体">的边表中。同时，在顺序表中，顶点</span><span style="font-family:Calibri">v</span><span style="font-family:宋体">除了存储顶点信息的数据域，还带有一个指针域，该指针指向</span><span style="font-family:Calibri">v</span><span style="font-family:宋体">的边表的第一个元素。如图</span><span style="font-family:Calibri">2</span><span style="font-family:宋体">中的邻接表中，</span><span style="font-family:Calibri">0</span><span style="font-family:宋体">号顶点的数据域存有数据</span><span style="font-family:Calibri">v0</span><span style="font-family:宋体">，指针域存有指针</span><span style="font-family:Calibri">P0</span><span style="font-family:宋体">，该指针指向</span><span style="font-family:Calibri">0</span><span style="font-family:宋体">号顶点的边表，该边表中存储了与</span><span style="font-family:Calibri">0</span><span style="font-family:宋体">号顶点相邻的所有顶点的编号，即</span><span style="font-family:Calibri">1</span><span style="font-family:宋体">号、</span><span style="font-family:Calibri">2</span><span style="font-family:宋体">号和</span><span style="font-family:Calibri">3</span><span style="font-family:宋体">号顶点。</span></span>

<span style=";font-family:宋体;font-size:16px"> </span>

<span style=";font-family:黑体;font-size:14px">数据结构表示</span>

<span style=";font-family:宋体;font-size:16px">前文提到，邻接表是使用顺序表和链表混合存储图的数据结构。</span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">typedef</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">struct</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">char</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> vertex;</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> degree;</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EdgeList edgelist;</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} VexNode; </span>

<span style=";font-family:黑体;font-size:12px"><span style="font-family:黑体">代码块</span>2</span>

<span style=";font-family:宋体;font-size:16px"> </span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">typedef</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">struct</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> VexNode vexs\[N\];</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> type;</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> vcount;</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} GraphList; </span>

<span style=";font-family:黑体;font-size:12px"><span style="font-family:黑体">代码块</span>3</span>

<span style=";font-family:宋体;font-size:16px"> </span>

<span style=";font-family:宋体;font-size:16px"><span style="font-family:宋体">上述代码为邻接表的数据结构</span>C语言代码，代码块2中共包含3个成员变量，代码块3中也有3个成员变量。代码块3中的vex\[N\]是用于存储顶点信息和该顶点对应的边表指针的顺序表，即图的顶点表，type是图的类型，vcount是图中顶点的个数。代码块2是每个顶点的数据结构，vertex是顶点的信息，degree是顶点的度，edgelist是顶点的边表指针。可以看出，顶点表是一个顺序表，而边表是一个链表。</span>

<span style=";font-family:Calibri;font-size:16px"> </span>

<a name="_Toc3892"></a><span style="font-family: 宋体;font-size: 16px">2.2.2 有向图的邻接表表示</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">有向图的邻接表分为两种，即出边表和入边表。出边表即把所有以某顶点</span>v为起点的弧的终点存储到v的边表中，入边表即把所有以某顶点v为终点的弧的起点存储到v的边表中。如下图，图4是图3中有向图的出边表，而图5是该有向图的入边表。其数据结构与的设计无向图完全一致。</span>

![图片6.png](../img/202203181647605105202059.png "图片6.png")<span style="font-family: 宋体;font-size: 16px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">3</span><span style=";font-family:黑体;font-size:13px"> <span style="font-family:黑体">有向图</span></span>

![图片7.png](../img/202203181647605116964395.png "图片7.png")<span style="font-family: 宋体;font-size: 16px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">4</span><span style=";font-family:黑体;font-size:13px"> <span style="font-family:黑体">有向图的出边表</span></span>

![图片8.png](../img/202203181647605126202616.png "图片8.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">5</span><span style=";font-family:黑体;font-size:13px"> <span style="font-family:黑体">有向图的入边表</span></span>

<a name="_Toc30729"></a><span style=";font-family:宋体;font-size:16px">2.2.3函数解析</span>

<span style=";font-family:黑体;font-size:14px"><span style="font-family:黑体">（</span>1）GraphList \*initGraphList();</span>

<span style=";font-family:宋体;font-size:16px">函数功能：初始化邻接表，并完成顶点和边信息的输入和保存。</span>

<span style=";font-family:宋体;font-size:16px">输入：图的类型、图的顶点数和边数；顶点信息；边的起始和终止顶点编号，以及该边的权值。</span>

<span style=";font-family:宋体;font-size:16px"><span style="font-family:宋体">返回值：初始化好，并且已经完成顶点和边输入极其存储的邻接表</span>GL。</span>

<span style=";font-family:宋体;font-size:16px">主要思路：</span>

<span style="font-family:宋体;font-size:16px">（1）</span><span style=";font-family:宋体;font-size:16px"><span style="font-family:宋体">初始化：创建一个邻接表对象，接收完图类型、顶点和边数输入后，将邻接表中每个顶点的入度初始化为</span>0；</span>

<span style="font-family:宋体;font-size:16px">（2）</span><span style=";font-family:宋体;font-size:16px"><span style="font-family:宋体">构建邻接表：</span>①输入点集并保存在顶点表中；</span>

<span style=";font-family:宋体;font-size:16px">②为每一个顶点申请一个边表存储空间；</span>

<span style=";font-family:宋体;font-size:16px">③输入边信息，用三个变量former、latter和weight分别存储边的起点下标、终点下标和权值；</span>

<span style=";font-family:宋体;font-size:16px">④根据输入的边的起点、终点把顶点v的邻接顶点插入到v的边表的头部。对于无向图，需要在下标为former的顶点的边表中插入latter，还要在下标为latter的顶点的边表中插入former。同时还要在边表的相应结点中存储v到该结点的边的权值。在边表结点中还要设置一个指针域用于指向下一个邻接顶点。对于有向图，则不需要在下标为latter的顶点的边表中插入former,其余与无向图一致。</span>

<span style=";font-family:宋体;font-size:16px"> </span>

<a name="_Toc3228"></a><span style="font-family: 黑体;font-size: 16px">2.3 图的度</span>

<span style="font-family: 黑体;font-size: 14px">数学表示</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">与顶点</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">相关联的边的条数。对于无向图，可分为入度和出度，以顶点</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">为起点的边的条数即为</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">的出度，以顶点</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">为终点的边的条数即为</span><span style="font-family:Calibri">V</span><span style="font-family:宋体">的入度。</span></span>

<span style="font-family: 宋体;font-size: 16px">2.3.1 邻接矩阵求度数</span>

![图片9.png](../img/202203181647605140933765.png "图片9.png")

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">矩阵</span>4</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">如上矩阵（矩阵</span>4）是图1无向图的邻接矩阵，由于邻接矩阵中的1表示某顶点vi与vj邻接，所以上述矩阵中的第i行（或第j列）的1的个数即为下标为i（或j）的顶点的度数。</span>

![图片10.png](../img/202203181647605150425772.png "图片10.png")

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">矩阵</span>5</span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">如上矩阵（矩阵</span>5）是图3有向图的邻接矩阵，由于邻接矩阵中的1表示图中存在某顶点vi到vj的有向边，所以上述矩阵中的第i行的1的个数即为下标为i的顶点的出度，第j列的1的个数即为下标为j的顶点的入度。</span>

<span style="font-family: 黑体;font-size: 14px">算法</span>

<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> vexs\[N\]\[N\]; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (</span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> i = 0; i < vexs.length; i++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> degree = 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (</span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> j = 0; j < vexs.length; j++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (vexs\[i\]\[j\]==1){ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> degree++; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%d\\n"</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">,degree); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">代码块</span>4 无向图矩阵求度数</span>

<span style="font-family: 黑体;font-size: 13px"> </span>

<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> vexs\[N\]\[N\]; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (</span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> i = 0; i < vexs.length; i++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> inCount = 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> outCount = 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (</span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> j = 0; j < vexs.length; j++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (vexs\[j\]\[i\]!=0&&i!=j){ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> inCount++; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (vexs\[i\]\[j\]!=0&&i!=j){ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> outCount++; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">13. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%d %d"</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">,inCount,outCount); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">14. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">代码块</span>5 有向图矩阵求度数</span>

<a name="_Toc12642"></a><span style="font-family: 宋体;font-size: 16px">2.3.2 邻接表求度数</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">邻接表求度数比较简单，如图</span>2无向图的邻接表中，求顶点vi的度数，只需查找vi的边表中顶点的个数即可。而对于图3有向图，要求顶点出度则到如图4的出边表中查找相应顶点的边表中顶点个数即可，要求顶点入度则到图5的入边表中查找相应顶点的边表中顶点个数即可。</span>

<span style="font-family: 黑体;font-size: 14px">算法</span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">void</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> function(GraphList GL) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> VexNode vexs\[\] = GL->vexs; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (</span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> i = 0; i < vexs.length; i++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> degree = 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EdgeList EL = GL->vexs\[i\].edgelist; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (EL!=NULL){ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> degree++; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EL = EL->nextedge; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%d\\n"</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">,degree); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} </span>

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">代码块</span>6 邻接表求度数</span>

<span style="font-family: 黑体;font-size: 14px"> </span>

<a name="_Toc27778"></a><span style="font-family: 黑体;font-size: 16px">2.4 两种存储方式的比较</span>

<span style="font-family: 宋体;font-size: 16px">邻接矩阵和邻接表各有优缺点，分别适合不同的场景。</span>

<table cellspacing="0" width="619"><tbody><tr class="firstRow" style="height:96px"><td style="padding: 0px 7px; border-width: 1px; border-color: windowtext;" valign="center" width="155"></td><td style="padding: 0px 7px; border-width: 1px; border-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">优点</span></td><td style="padding: 0px 7px; border-width: 1px; border-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">缺点</span></td><td style="padding: 0px 7px; border-width: 1px; border-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">适用场景</span></td></tr><tr style="height:99px"><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">邻接矩阵</span></td><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">①快速确定两点之间是否有边；</span><span style="font-family: 宋体;font-size: 16px">②快速添加、删除边</span></td><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">在存储稀疏图时浪费的空间较多</span></td><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">稠密图（边数</span>e>nlog(2)n）</span></td></tr><tr style="height:99px"><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">邻接表</span></td><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">节省空间，之存储存在的边</span></td><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px">求顶点的度时，需要遍历整个链表</span></td><td style="padding: 0px 7px; border-left-width: 1px; border-left-color: windowtext; border-right-width: 1px; border-right-color: windowtext; border-top: none; border-bottom-width: 1px; border-bottom-color: windowtext;" valign="center" width="155"><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">稀疏图（边数</span>e<nlog></nlog></span></td></tr></tbody></table>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">表</span> </span><span style=";font-family:Arial;font-size:13px">1</span><span style=";font-family:黑体;font-size:13px"> <span style="font-family:黑体">两种存储方式的比较</span></span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<a name="_Toc17569"></a><span style="font-family: 黑体;font-size: 16px">2.5 带权图</span>

<span style="font-family: 宋体;font-size: 16px">图中每条边赋予相应权值的图称为带权图（赋权图）。</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">若图用邻接矩阵存储，则直接将矩阵中的</span>1改为相应边上的权值即可；若用邻接表存储，则在边表的相应邻接结点上存储相应权值即可。对于无向图，(vi,vj)的权值和(vj,vi)的权值相同。</span>

<a name="_Toc16146"></a><span style="font-family: 黑体;font-size: 19px">三、</span><span style="font-family: 黑体;font-size: 19px">图的遍历</span>

<a name="_Toc24131"></a><span style="font-family: 黑体;font-size: 16px">3.1 广度优先遍历</span>

<a name="_Toc29208"></a><span style="font-family: 宋体;font-size: 16px">3.1.1 算法分析与方法选择</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">广度优先遍历是遍历图中的顶点时，优先遍历某顶点的所有邻接顶点的算法。如图</span>1中从顶点v0开始的广度优先遍历结果为（v0,v1,v3,v2），从v1开始的广度优先遍历结果为（v1,v0,v2,v3）。可见，广度优先遍历遇到顶点时，总是会先把当前顶点和它邻接的所有顶点遍历完，再跳到它所遍历的第一个邻接顶点上，重复上述操作。这种方式的特点和队列的特点类似。所以可以考虑使用队列来完成遍历。如图，右边的是队列，上面是队头，下面是队尾。</span>

<a name="_Toc19344"></a><span style="font-family: 黑体;font-size: 14px">广度优先遍历过程图示图示</span>

![图片11.png](../img/202203181647605162884036.png "图片11.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">6</span>

![图片12.png](../img/202203181647605172482980.png "图片12.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">7</span>

![图片13.png](../img/202203181647605186816075.png "图片13.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">8</span>

![图片14.png](../img/202203181647605197715630.png "图片14.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">9</span>

![图片15.png](../img/202203181647605210290721.png "图片15.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">10</span>

<span style=";font-family:宋体;font-size:14px"> </span>

<span style="font-family: 黑体;font-size: 14px">算法</span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">1. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> \*visited = makeFlag(G->vcount); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> v = 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> Q\[20\];</span><span style="font-family: Consolas;color: #008200;letter-spacing: 0;font-size: 9px">//顺序队列</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> front, rear; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> front = rear = -1; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">struct</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EdgeNode \*p; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%c "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">, G->vexs\[0\].vertex); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> visited\[v\] = 1; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> Q\[rear++\] = v;</span><span style="font-family: Consolas;color: #008200;letter-spacing: 0;font-size: 9px">//已访问结点入队</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> t; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (front != rear) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> v = Q\[front++\];</span><span style="font-family: Consolas;color: #008200;letter-spacing: 0;font-size: 9px">//结点出队</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">13. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> p = G->vexs\[v\].edgelist; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">14. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (p) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">15. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> t = p->endvex; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">16. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (visited\[t\] == 0) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">17. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%c "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">, G->vexs\[t\].vertex); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">18. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> visited\[t\] = 1; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">19. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> Q\[rear++\] = t;</span><span style="font-family: Consolas;color: #008200;letter-spacing: 0;font-size: 9px">//已访问结点入队</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">20. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">21. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> p = p->nextedge; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">22. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">23. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">24. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} </span>

<span style="font-family: 黑体;font-size: 12px"><span style="font-family:黑体">代码块</span>7</span>

<a name="_Toc1204"></a><span style="font-family: 黑体;font-size: 16px">3.2 深度优先遍历</span>

<a name="_Toc15185"></a><span style="font-family: 宋体;font-size: 16px">3.2.1 算法分析与方法选择</span>

<span style="font-family: 宋体;font-size: 16px">深度优先遍历是在遍历图中的顶点时，优先持续向下遍历直到下一个为空的算法。</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">如下图，从</span>v0开始的深度优先遍历结果为(v0,v1,v3,v2,v4)，从v1开始的深度优先遍历结果为（v1,v3,v2,v4,v0）。可见，深度优先遍历在遍历图中的顶点时，总是先持续向下遍历，直到下一个为空时，再一步步回头遍历前面遍历过的顶点的邻接顶点。这个特点和栈的特点很相似，所以可以考虑使用栈或者递归来完成遍历。</span>

![图片16.png](../img/202203181647605221581809.png "图片16.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">11</span>

<span style="font-family: 黑体;font-size: 14px">深度优先遍历过程图示图示</span>

![图片17.png](../img/202203181647605229993383.png "图片17.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">12</span>

![图片18.png](../img/202203181647605238895060.png "图片18.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">13</span>

![图片19.png](../img/202203181647605245592157.png "图片19.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">14</span>

![图片20.png](../img/202203181647605254766443.png "图片20.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">15</span>

![图片21.png](../img/202203181647605262962734.png "图片21.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">16</span>

![图片22.png](../img/202203181647605270739847.png "图片22.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">17</span>

<a name="_Toc6478"></a><span style="font-family: 宋体;font-size: 16px">3.2.2 递归法</span>

<span style="font-family: 黑体;font-size: 14px">算法主要代码</span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">void</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> DFS(GraphList *G,* </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> i, </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> visited) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> visited\[i\] = 1; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%c "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">, G->vexs\[i\].vertex); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">struct</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EdgeNode \*p = G->vexs\[i\].edgelist; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (p) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (!visited\[p->endvex\]) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> DFS(G, p->endvex, visited); </span><span style="font-family: Consolas;color: #008200;letter-spacing: 0;font-size: 9px">//递归深度遍历</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> p = p->nextedge; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} </span>

<span style="font-family: 黑体;font-size: 14px"> </span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">void</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> DFS\_list(GraphList \*G) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> \*visited = makeFlag(G->vcount); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> i; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (i = 0; i < G->vcount; i++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> visited\[i\] = 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (i = 0; i < G->vcount; i++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (visited\[i\] != 1) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> DFS(G, i, visited); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">13. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} </span>

<a name="_Toc16905"></a><span style="font-family: 宋体;font-size: 16px">3.2.3 非递归法（栈法）</span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">void</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> DFS\_list(GraphList \*G) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span><span style="font-family: Consolas;color: #008200;letter-spacing: 0;font-size: 9px">//非递归法（栈），卒！</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> Stack\[20\]; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> top = -1; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">struct</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EdgeNode \*p; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> v = 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> \*visited = makeFlag(G->vcount); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> t; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%c "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">,G->vexs\[0\].vertex); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> visited\[v\] = 1; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> Stack\[top+1\] = v; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> top++; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">13. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (top!=-1){ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">14. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> v = Stack\[top\]; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">15. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> p = G->vexs\[v\].edgelist; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">16. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (p){ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">17. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"while"</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">18. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> t = p->endvex; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">19. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (visited\[t\]==0){ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">20. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"66 "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">21. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">22. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%c "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">,G->vexs\[t\].vertex); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">23. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"77 "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">24. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> visited\[t\] = 1; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">25. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"88 "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">26. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> Stack\[top++\] = t;</span><span style="font-family: Consolas;color: #008200;letter-spacing: 0;font-size: 9px">//已访问结点入栈</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">27. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"\[%d %d\] "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">,top,t); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">28. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">29. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> p = p->nextedge; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">30. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">31. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">32. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} </span>

<span style="font-family: 宋体;font-size: 16px"> </span>

<a name="_Toc26416"></a><span style="font-family: 黑体;font-size: 19px">四、</span><span style="font-family: 黑体;font-size: 19px">拓扑排序</span>

<a name="_Toc9064"></a><span style="font-family: 黑体;font-size: 16px">4.1 算法分析</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">拓扑排序是一个有向无环图的所有顶点的线性序列，每个顶点再序列中仅出现一次，且如果序列中存在顶点</span>v0到v1的路径，那么在序列中v0必定出现在v1之前。</span>

<span style="font-family: 宋体;font-size: 16px">拓扑排序的算法思想如下：</span>

<span style="font-family: 宋体;font-size: 16px">1. </span><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">在一个有向图中，选择一个入度为</span>0的顶点，将该顶点输出；</span>

<span style="font-family: 宋体;font-size: 16px">2. </span><span style="font-family: 宋体;font-size: 16px">从图中删除该顶点以及所有以该顶点为起点的有向边。</span>

<span style="font-family: 宋体;font-size: 16px">3. </span><span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">重复</span>1和2，直到输出完所有顶点为止。</span>

![图片23.png](../img/202203181647605278918531.png "图片23.png")<span style=";font-family:Calibri;font-size:14px"> </span>

<span style=";font-family:Arial;font-size:13px"><span style="font-family:黑体">图</span> </span><span style=";font-family:Arial;font-size:13px">18</span>

<span style=";font-family:宋体;font-size:16px"><span style="font-family:宋体">如图</span>18所示，该图的拓扑排序序列为（v1,v2,v4,v3,v5）。</span>

<span style=";font-family:黑体;font-size:14px">算法主要代码</span>

<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">void</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> Top\_list(GraphList \*G) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">for</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (</span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> i = 0; i < G->vcount; i++) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (G->vexs\[i\].degree == 0) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> printf(</span><span style="font-family: Consolas;color: #0000FF;letter-spacing: 0;font-size: 9px">"%c "</span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">, G->vexs\[i\].vertex); </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EdgeList EL = G->vexs\[i\].edgelist; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (EL != NULL) { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> G->vexs\[EL->endvex\].degree--; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EL = EL->nextedge; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">13. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} </span>

<span style=";font-family:黑体;font-size:14px"> </span>

<a name="_Toc3756"></a><span style="font-family: 黑体;font-size: 16px">4.2 应用</span>

<span style="font-family: 宋体;font-size: 16px">拓扑排序常用于解决有依赖关系的复杂任务。比如大学生选修课程的现后顺序，使用拓扑排序就可以得到满足课程依赖关系的选修顺序。又比如工程项目，很多工程项目是需要前面的先完成，后面的才能做的，使用拓扑排序就可以排出正确的施工顺序。</span>

<a name="_Toc17484"></a><span style="font-family: 黑体;font-size: 19px">五、</span><span style="font-family: 黑体;font-size: 19px">最小生成树</span>

<span style="font-family: 宋体;font-size: 16px"><span style="font-family:宋体">最小生成树是一个包含原图所有顶点，且边最少的连通图子图。有</span>n个顶点的图的最小生成树中有n-1条边。</span>

<span style="font-family: 宋体;font-size: 16px">求最小生成树的算法有克鲁斯卡尔算法和普里姆算法，其中普里姆算法较常用。</span>

<span style="font-family: 黑体;font-size: 14px">算法步骤</span>

<span style="font-family: 黑体;font-size: 14px">（1）</span><span style="font-family: 黑体;font-size: 14px"><span style="font-family:黑体">输入：一个加权连通图，其中顶点集合为</span>V，边集合为E；</span>

<span style="font-family: 黑体;font-size: 14px">（2）</span><span style="font-family: 黑体;font-size: 14px"><span style="font-family:黑体">初始化：</span>Vnew= {x}，其中x为集合V中的任一节点（起始点），Enew= {},为空；</span>

<span style="font-family: 黑体;font-size: 14px">（3）</span><span style="font-family: 黑体;font-size: 14px"><span style="font-family:黑体">重复下列操作，直到</span>Vnew= V：</span>

<span style="font-family: 黑体;font-size: 14px">a.在集合E中选取权值最小的边<u, v>，其中u为集合Vnew中的元素，而v不在Vnew集合当中，并且v∈V（如果存在有多条满足前述条件即具有相同权值的边，则可任意选取其中之一）；</span>

<span style="font-family: 黑体;font-size: 14px">b.将v加入集合Vnew中，将<u, v>边加入集合Enew中；</span>

<span style="font-family: 黑体;font-size: 14px">（4）</span><span style="font-family: 黑体;font-size: 14px"><span style="font-family:黑体">输出：使用集合</span>Vnew和Enew来描述所得到的最小生成树。</span>

<span style="font-family: 黑体;font-size: 14px">算法代码</span>

<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-weight: bold;font-size: 16px">1. </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> getWeight(GraphList G, </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> start, </span>**<span style="font-family: Consolas;color: #2E8B57;letter-spacing: 0;font-size: 9px">int</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> end) </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">2. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">{ </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">3. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">struct</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> EdgeNode \*node; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">4. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">5. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (start==end) </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">6. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">return</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> 0; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">7. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">8. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> node = G.vexs\[start\].edgelist->nextedge; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">9. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">while</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (node!=NULL) </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">10. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> { </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">11. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">if</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> (end==node->endvex) </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">12. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">return</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> node->weight; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">13. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> node = node->nextedge; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">14. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> } </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">15. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">16. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> </span>**<span style="font-family: Consolas;color: #006699;letter-spacing: 0;font-size: 9px">return</span>**<span style="font-family: Consolas;letter-spacing: 0;font-size: 9px"> 10000; </span>

<span style="font-family: Consolas;letter-spacing: 0;font-size: 16px">17. </span><span style="font-family: Consolas;letter-spacing: 0;font-size: 9px">} </span>