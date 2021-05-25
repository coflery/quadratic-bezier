# Quadratic Bezier

Demo of quadratic bezier through three points, refer to: [http://xuhehuan.com/2608.html](http://xuhehuan.com/2608.html).

Demo URL: [http://github.xuhehuan.com/quadratic-bezier/quadratic-bezier.html](http://github.xuhehuan.com/quadratic-bezier/quadratic-bezier.html)

# Distance to a Quadratic Bezier Curve

Demo of the distance to a quadratic bzier curve, refer to: [http://blog.gludion.com/2009/08/distance-to-quadratic-bezier-curve.html](http://blog.gludion.com/2009/08/distance-to-quadratic-bezier-curve.html).

Demo URL: [http://github.xuhehuan.com/quadratic-bezier/Bezier_03.swf](http://github.xuhehuan.com/quadratic-bezier/Bezier_03.swf)

Source Code: [http://github.xuhehuan.com/quadratic-bezier/Bezier.as](http://github.xuhehuan.com/quadratic-bezier/Bezier.as)


贝塞尔曲线（Bézier curve）是计算机图形学中相当重要的参数曲线，Photoshop 中的钢笔效果，Flash5 的贝塞尔曲线工具都是它在计算机图形学中的具体应用。 贝塞尔曲线由法国雷诺汽车公司的工程师皮埃尔·贝塞尔（Pierre Bézier）于 1962 年所广泛发表，主要用来为汽车的主体进行设计，并且由于他给出了详细的计算公式，因此按照这样的公式绘制出来的曲线就用他的姓氏来命名。贝塞尔曲线由一系列的关键点来控制曲线的状态，这些关键点又可以分为两类，分别是端点和控制点：端点确定曲线的起始和结束位置， 控制点确定曲线的弯曲程度。由n+1 个控制点定义的贝塞尔曲线称为n次贝塞尔曲线。这里以二次贝塞尔曲线为例。

其中P0, P2为端点，P1为控制点，正常的贝塞尔曲线是不通过P1控制点的，因此我们的目标是希望找到一个新的点PC，使得由P0, Pc, P2点构造的贝塞尔曲线过P1点，如下示意图。

这里不说过程，只写结果了，最终PC点的坐标为：

具体推导过程见 Gabriel Suchowolski 的论文 Quadratic bezier through three points，我用 HTML5 的 canvas 标签实现了个网页上的 demo，开源到了 Github 上，效果见： http://github.xuhehuan.com/quadratic-bezier/quadratic-bezier.html，可随意拖动三点的位置，查看变形效果。

另外，根据贝塞尔曲线的性质：n次贝塞尔曲线可以转换为一个形状完全相同的n+1次贝塞尔曲线，具体见维基百科贝塞尔曲线升阶，据此可以将二次贝塞尔曲线转换成对应的三次贝塞尔曲线，新的端点和控制点分别为：

这样可以增大曲线调整的灵活性， 在某些只支持特定阶次贝塞尔曲线的软件中很有用 。
