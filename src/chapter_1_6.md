# 效率

<br/>
&emsp;&emsp;并没有什么神奇的规则能够使代码更加高效。高效性是通过仔细的权衡来实现的，而这些权衡对于不同的架构是不同的。然而，在可预见的未来，一个好的启发式方法是，程序员应该更多地关注内存访问模式而不是操作数。这与20年前的最佳启发式方法相反。出现这种转变是因为内存的速度没有跟上处理器的速度。由于这一趋势仍在继续，有限和连贯的内存访问对优化的重要性应该只会增加。

&emsp;&emsp;一个合理的使代码快速化的方法是按以下顺序进行，只采取那些需要的步骤：

1. 尽可能以最直接的方式编写代码。根据需要即时计算中间结果而不是存储它们；
2. 在优化模式下进行编译；
3. 使用现有的任何分析工具来找到关键瓶颈；
4. 检查数据结构以寻找改善局部性的方法。如果可能，使数据单元大小与目标架构上的缓存/页面大小相匹配；
5. 如果分析揭示了数值计算的瓶颈，请检查编译器生成的汇编代码是否存在效率缺失。重写源代码以解决发现的任何问题。

&emsp;&emsp;在这些步骤中最重要的是第一个步骤。大多数的 "优化 "使代码更难读，但却没有加快速度。此外，前期花在优化代码上的时间通常更适合用来纠正错误或增加功能。另外，要注意旧文本中的建议；一些经典的技巧，如使用整数而不是实数，可能不再产生速度，因为现代的CPU通常在执行浮点数操作时像执行整数操作一样快。在所有情况下都应该进行分析，以确定任何优化对特定机器和编译器的好处。
