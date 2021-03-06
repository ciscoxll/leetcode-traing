**问题**

给定一个由整数组成的非空数组所表示的非负整数，在该数的基础上加一。

最高位数字存放在数组的首位， 数组中每个元素只存储一个数字。

你可以假设除了整数 0 之外，这个整数不会以零开头。
示例 1:

输入: [1,2,3]
输出: [1,2,4]
解释: 输入数组表示数字 123。
示例 2:

输入: [4,3,2,1]
输出: [4,3,2,2]
解释: 输入数组表示数字 4321。

**思路**

1. 首先根据题意，输入的数组表示的数加一。

2. 假如不是要增加数组长度的分为一类，要增加数组长度的分为一类。从最后一位开始进位只要这一位是9就将这一位变为0，然后继续向前遍历（倒数第二位），假如这位不是9则这一位就加一跳出循环，拷贝到malloc动态开辟的数组中去。

3. 如果是继续为0，再遍历下一位，直到遍历结束。假如结束后第一位是0则增加一位为1，其余全是0，增长数组长长度。
