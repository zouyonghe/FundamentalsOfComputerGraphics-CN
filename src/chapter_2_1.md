# 集合和映射

<br/>

&emsp;&emsp;映射，也叫函数，是数学和编程的基础。像程序中的函数一样，数学中的映射需要同一个类型的参数，并将其映射到（返回）一个特定类型的对象。在程序中，我们说的是 "类型"；在数学中，我们要确定集合。当我们有一个对象是一个集合的成员时，我们使用∈符号。比如说，

a ∈ S，

可以理解为 "a是集合S的成员"。给定任何两个集合A和B，我们可以通过两个集合的笛卡尔积来创建第三个集合，表示为A×B。这个集合A×B由所有可能的有序对（a，b）组成，其中a∈A和b∈B。作为缩写，我们用符号A^2表示A×A。我们可以扩展笛卡尔积，从三个集合中创建一个所有可能的有序三元组集合，以此类推，从任意多的集合中创建任意长的有序元组。

&emsp;&emsp;常见的关注点包括：
- $\mathbb{R}$——实数；
- $\mathbb{R^+}$——非负实数（包括0）；
- $\mathbb{R}^2$——真实二维平面中的有序对；
- $\mathbb{R}^n$——n维迪卡尔空间中的点；
- $\mathbb{Z}$——整数；
- $S^2$——单位球面上的三维点（R^3中的点）的集合。

&emsp;&emsp;请注意，虽然S^2是由嵌入三维空间的点组成的，但它是在一个可以用两个变量进行参数化的表面上，所以它可以被认为是一个二维集合。对映射的记号使用箭头和冒号，例如，

$$
f : \mathbb{R} \mapsto \mathbb{Z},
$$

你可以把它理解为 "有一个叫做f的函数，它把一个实数作为输入，并把它映射成一个整数。" 这里，箭头前面的集合被称为函数的域，右边的集合被称为目标。计算机程序员可能更愿意使用下面等价的语句。"有一个叫f的函数，它有一个实数参数，返回一个整数"。换句话说，上面的集合符号等同于常见的编程符号：
$$
\text{integer} \  f(\text{real}) \leftarrow \text{equivalent} \rightarrow f : \mathbb{R} \mapsto \mathbb{Z}。
$$
因此，冒号符号可以被认为是一种编程语法。就是这么简单。

&emsp;&emsp;点f(a)被称为a的映像，一个集合A（定义域的子集）的映像是目标映像的子集，包含A中所有点的映像。整个定义域的映像被称为函数的值域。

## 逆向映射

&emsp;&emsp;如果我们有一个函数f : A->B，可能存在一个反函数f^-1 : B->A，它的定义是当b = f ( a )时，f^-1 ( b ) = a 。这个定义只有在每个b \in B都是f下某个点的图像（即范围等于目标），并且只有一个这样的点（即只有一个a，f(a)=b）时才有效。这样的映射或函数被称为双投。双投将每一个a E A映射到一个唯一的b E B，对于每一个b E B，正好有一个a E A，使f(a)=b（图2.1）。一组骑手和马匹之间的双射关系表明，每个人都骑着一匹马，每匹马都被骑着。这两个函数是骑手（马）和马（骑手），它们是彼此的反函数。不是双射的函数没有反函数（图2.2）。

![2.1](./img/2.1.png)

![2.2](./img/2.2.png)