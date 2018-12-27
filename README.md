关于goNum
==========
goNum是一款完全以[Go](https://golang.org)语言为基础的开源数值算法库，它可以使你像调用其它go函数一样使用其进行数值运算，且不依赖于任何外部库。
限于作者业余时间有限，目前功能还在一步步完善，算法还在慢慢添加。
绝大部分算法进行了典型状态测试，但不保证所有算法在所有状态下都是安全的、可靠的。
另外，需要注意的是，此算法库旨在解决问题，而不是实现语言的某些能力，即使作者正在努力使得go语言的独特性在其中充分体现。
如果您对作者的工作满意，请留心关注goNum的更新状态；如果您对作者的工作有所建议，请电邮：chengfengcool@sina.com。
或者，承蒙赏识，如果您愿意捐助关于goNum工作，请电邮联系作者。

欢迎有志之士加入开发。

安装环境
=========
Linux或者Windows
1. go 1.11（推荐）或更新版本;
2. [可选] LiteIDE X34或更新版本;
3. 请关注Linux和Windows换行符的区别。

安装方法
=========
## 1. 在线安装
1. 安装go;
2. 运行go get命令:
```go
go get github.com/chfenger/goNum
```
## 2. 下载源码安装
1. 下载源代码，并解压到指定文件夹（例如“UserDir”）下的src目录或其子目录（例如“UserDir/src/”或“UserDir/src/xxx/xxx/”）下;
2. 添加UserDir到GOPATH;
3. 重启IDE或终端即可。

关于命名
==========
1. 包名'goNum'为算法库包;
2. 包名'goNum_test'为测试库包（Benchmark）;
3. 文件名'*_test.go'为测试文件名，其内容可作为算法包使用的参考手册。

设计初衷
=========
1. 旨在为自己和他人提供一个浅显易懂而又功能强大的数值算法库;
2. 优先保证速度和精度，因此诸如defer等优秀方式由于过于影响速度而并未实际采用;
3. 完全以Go语言开发，独立而不依赖于任何外部库。

算法
=====
（持续更新中...）
- 基本数学
  - 排列
  - 二分法
  - 组合
  - 阶乘
  - 切片元素最大值
  - 切片元素绝对值最大值
  - 切片元素从大到小排序
  - 切片元素最小值
  - 切片元素绝对值最小值
  - 切片元素从小到大排序
  - 矩阵1范数
  - 矩阵无穷范数
  - 向量的范数
  - 次幂扩展
  - 角度的三角函数和反三角函数
  - 向量在三维空间的旋转
  - Fibonacci数列
  - 多项式求导

- 矩阵
  - 矩阵定义与操作
  - 求矩阵行列式的列主元消去法
  - 返回n阶单位矩阵（二维切片表示）
  - 求矩阵逆的列主元消去法
  - 求对称正定矩阵的平方根分解法
  - 求矩阵Doolittlede LU分解
  - 求对称矩阵全部特征值及其特征向量，经典雅可比法
  - 求对称矩阵全部特征值及其特征向量，雅可比过关法
  - 求矩阵A的主特征值及其特征向量

- 解一般方程
  - 求解非线性方程的牛顿迭代
  - 搜索法求方程解
  - 单点弦截法
  - 双点弦截法
  - 简单迭代求解类x=g(x)方程的解
  - 简单迭代求解类x=g(x)方程的解（Aitken加速）
  - Muller法求f(x)=0的解

- 插值
  - Hermite插值
  - Hermite插值函数
  - Lagrange插值
  - Lagrange插值函数
  - Newton插值
  - Newton前向插值
  - 用节点处的一阶导数表示的三次样条插值函数（一阶导数边界条件）
  - 用节点处的一阶导数表示的三次样条插值函数（二阶导数边界条件）
  - 用节点处的二阶导数表示的三次样条插值函数（一阶导数边界条件）
  - 用节点处的二阶导数表示的三次样条插值函数（二阶导数边界条件）

- 数值积分
  - 1-8级复化Newton-Cotes求积分公式
  - 1-8级逐次分半复化Newton-Cotes求积分公式
  - 不超过8次的Gauss-Lagendre求积分公式
  - 1-8级Newton-Cotes求积分公式
  - Rumberg(龙贝格)求积分公式

- 解线性方程组
  - 求解矛盾方程组的最小二乘法
  - 追赶法求解严格对角占优的三对角系数矩阵方程组
  - 线性代数方程组的列主元消去法
  - 解n阶线性方程组的Jocobi迭代法（简单迭代法）
  - 解n阶线性方程组的Seidel迭代法
  - 解n阶线性方程组的SOR(逐次超松弛)迭代法

- 解非线性方程组
  - 多元非线性方程组Seidel迭代

- 数据拟合
  - 多项式拟合
  - 线性最小二乘拟合
  - Bezier曲线拟合控制点

- 误差评估
  - 最大误差
  - 平均误差
  - 均方根误差

- 优化
  - 黄金分割法求单峰单自变量极小值
  - Fibonacci搜索法求单峰单自变量极小值
  - 单纯形法求多自变量函数极小值

- 常微分方程
  - 4步Adams外推（ODE）
  - 三步Adams内插公式（ODE）
  - Euler法（ODE）
  - Euler预估校正（ODE）
  - 梯形法（ODE）
  - 二级二阶Runge-Kutta法
  - 四级四阶Runge-Kutta法
  - 四阶Runge-Kutta-Fehlberg变步长
  - Heun法

- 偏微分方程
  - 双曲型偏微分方程差分解法（第一种差分格式）
  - 双曲型偏微分方程差分解法（第二种差分格式）
  - 抛物型偏微分方程差分解法（显式）
  - 抛物型偏微分方程差分解法（隐式）
  - 抛物型偏微分方程差分解法（六点对称）

作者
=====
详见AUTHOR.MD文件

许可证书
=========
goNum是一款开源自由算法库，您可以根据自己的需求发布或者修改，但这一切需要在GNU GPL(General Public License) v3.0
或者较新版本的许可下进行。关于此许可证内容详见根目录下LICENSE文件或者<http://www.gnu.org/licenses/>。

程锋 版权所有 2018

致谢
=====
00. 非常感谢家人朋友们的支持和理解，为此推辞了许多业余活动.
01. 特别感谢Google提供如此美妙的编程语言，希望再接再励，继续改善使之丰富。
10. 感谢某实验室提供的免费服务器。


