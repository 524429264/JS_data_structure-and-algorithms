# 排序算法

## 冒泡排序
冒泡排序（Bubble Sort，台湾译为：泡沫排序或气泡排序）是一种简单的排序算法。它重复地走访过要排序的数列，一次比较两个元素，如果他们的顺序错误就把他们交换过来。走访数列的工作是重复地进行直到没有再需要交换，也就是说该数列已经排序完成。

### 思想


冒泡排序算法的运作如下：（从后往前）

1.比较相邻的元素。如果第一个比第二个大，就交换他们两个。

2.对每一对相邻元素作同样的工作，从开始第一对到结尾的最后一对。在这一点，最后的元素应该会是最大的数。

3.针对所有的元素重复以上的步骤，除了最后一个。

4.持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。

![](http://onnq25vz1.bkt.clouddn.com/t0116a956da6607091c.png)



### 详细介绍



冒泡排序（BubbleSort）的基本概念是：依次比较相邻的两个数，将小数放在前面，大数放在后面。即在第一趟：首先比较第1个和第2个数，将小数放前，大数放后。然后比较第2个数和第3个数，将小数放前，大数放后，如此继续，直至比较最后两个数，将小数放前，大数放后。


至此第一趟结束，将最大的数放到了最后。在第二趟：仍从第一对数开始比较（因为可能由于第2个数和第3个数的交换，使得第1个数不再小于第2个数），将小数放前，大数放后，一直比较到倒数第二个数（倒数第一的位置上已经是最大的），第二趟结束，在倒数第二的位置上得到一个新的最大数（其实在整个数列中是第二大的数）。如此下去，重复以上过程，直至最终完成排序。


### 实例

![](http://onnq25vz1.bkt.clouddn.com/maopao.png)

## 选择排序
选择排序(Selection sort)是一种简单直观的排序算法。它的工作原理是每一次从待排序的数据元素中选出最小(或最大)的一个元素，存放在序列的起始位置，直到全部待排序的数据元素排完。 选择排序是不稳定的排序方法(比如序列[5， 5， 3]第一次就将第一个[5]与[3]交换，导致第一个5挪动到第二个5后面)。

不稳定的排序方法

### 算法原理

①初始状态:无序区为R[1..n]，有序区为空。

②第1趟排序

在无序区R[1..n]中选出关键字最小的记录R[k]，将它与无序区的第1个记录R[1]交换，使R[1..1]和R[2..n]分别变为记录个数增加1个的新有序区和记录个数减少1个的新无序区。

……

③第i趟排序

第i趟排序开始时，当前有序区和无序区分别为R[1..i-1]和R(i..n)。该趟排序从当前无序区中选出关键字最小的记录 R[k]，将它与无序区的第1个记录R交换，使R[1..i]和R分别变为记录个数增加1个的新有序区和记录个数减少1个的新无序区。

### 实例

![](http://onnq25vz1.bkt.clouddn.com/xuanze.png)

## 插入排序

有一个已经有序的数据序列，要求在这个已经排好的数据序列中插入一个数，但要求插入后此数据序列仍然有序，这个时候就要用到一种新的排序方法--插入排序法,插入排序的基本操作就是将一个数据插入到已经排好序的有序数据中，从而得到一个新的、个数加一的有序数据，算法适用于少量数据的排序，时间复杂度为O(n^2)。是稳定的排序方法。插入算法把要排序的数组分成两部分:第一部分包含了这个数组的所有元素，但将最后一个元素除外(让数组多一个空间才有插入的位置)，而第二部分就只包含这一个元素(即待插入元素)。在第一部分排序完成后，再将这个最后元素插入到已排好序的第一部分中。

插入排序的基本思想是:每步将一个待排序的纪录，按其关键码值的大小插入前面已经排序的文件中适当位置上，直到全部插入完为止。

稳定的



### 思想
将n个元素的数列分为已有序和无序两个部分，如下所示：

![](http://onnq25vz1.bkt.clouddn.com/t010d0bfc512300aa32.jpg)

{{a1}，{a2，a3，a4，…，an}}

{{a1⑴，a2⑴}，{a3⑴，a4⑴ …，an⑴}}

…

{{a1(n-1），a2(n-1) ，…},{an(n-1)}}

每次处理就是将无序数列的第一个元素与有序数列的元素从后往前逐个进行比较，找出插入位置，将该元素插入到有序数列的合适位置中。

### 算法描述

一般来说，插入排序都采用in-place在数组上实现。具体算法描述如下：

⒈ 从第一个元素开始，该元素可以认为已经被排序

⒉ 取出下一个元素，在已经排序的元素序列中从后向前扫描

⒊ 如果该元素（已排序）大于新元素，将该元素移到下一位置

⒋ 重复步骤3，直到找到已排序的元素小于或者等于新元素的位置

⒌ 将新元素插入到下一位置中

⒍ 重复步骤2

## 希尔排序
希尔排序(Shell Sort)是插入排序的一种。是针对直接插入排序算法的改进。该方法又称缩小增量排序，因DL．Shell于1959年提出而得名。

### 思想

先取一个小于n的整数d1作为第一个增量，把文件的全部记录分成d1个组。所有距离为dl的倍数的记录放在同一个组中。先在各组内进行直接插人排序；然后，取第二个增量d2<d1重复上述的分组和排序，直至所取的增量dt=1(dt<dt-l<…<d2<d1)，即所有记录放在同一组中进行直接插入排序为止。

希尔排序是不稳定的

该方法实质上是一种分组插入方法。


增量序列的取值依次为：

3，2，1

![](http://onnq25vz1.bkt.clouddn.com/t01b4af3cd6752197ab.png)


### 实例
![](http://onnq25vz1.bkt.clouddn.com/xier.png)


## 归并排序
归并排序（MERGE-SORT）是建立在归并操作上的一种有效的排序算法,该算法是采用分治法（Divide and Conquer）的一个非常典型的应用。将已有序的子序列合并，得到完全有序的序列；即先使每个子序列有序，再使子序列段间有序。若将两个有序表合并成一个有序表，称为二路归并。

归并过程为：比较a[i]和a[j]的大小，若a[i]≤a[j]，则将第一个有序表中的元素a[i]复制到r[k]中，并令i和k分别加上1；否则将第二个有序表中的元素a[j]复制到r[k]中，并令j和k分别加上1，如此循环下去，直到其中一个有序表取完，然后再将另一个有序表中剩余的元素复制到r中从下标k到下标t的单元。归并排序的算法我们通常用递归实现，先把待排序区间[s,t]以中点二分，接着把左边子区间排序，再把右边子区间排序，最后把左区间和右区间用一次归并操作合并成有序的区间[s,t]。


稳定排序算法

### 算法描述

归并操作的工作原理如下：
第一步：申请空间，使其大小为两个已经排序序列之和，该空间用来存放合并后的序列
第二步：设定两个指针，最初位置分别为两个已经排序序列的起始位置
第三步：比较两个指针所指向的元素，选择相对小的元素放入到合并空间，并移动指针到下一位置
重复步骤3直到某一指针超出序列尾
将另一序列剩下的所有元素直接复制到合并序列尾

### 归并操作编辑

归并操作(merge)，也叫归并算法，指的是将两个顺序序列合并成一个顺序序列的方法。
如　设有数列{6，202，100，301，38，8，1}
初始状态：6,202,100,301,38,8，1
第一次归并后：{6,202},{100,301},{8,38},{1}，比较次数：3；
第二次归并后：{6,100,202,301}，{1,8,38}，比较次数：4；
第三次归并后：{1,6,8,38,100,202,301},比较次数：4；
总的比较次数为：3+4+4=11,；
逆序数为14；


### 实例

![](http://onnq25vz1.bkt.clouddn.com/xier.png)

## 快速排序

快速排序由C. A. R. Hoare在1962年提出。它的基本思想是:通过一趟排序将要排序的数据分割成独立的两部分，其中一部分的所有数据都比另外一部分的所有数据都要小，然后再按此方法对这两部分数据分别进行快速排序，整个排序过程可以递归进行，以此达到整个数据变成有序序列。

快速排序（Quicksort）有几个值得一提的变种算法，这里进行一些简要介绍：

随机化快排：快速排序的最坏情况基于每次划分对主元的选择。基本的快速排序选取第一个元素作为主元。这样在数组已经有序的情况下，每次划分将得到最坏的结果。一种比较常见的优化方法是随机化算法，即随机选取一个元素作为主元。这种情况下虽然最坏情况仍然是O(n^2），但最坏情况不再依赖于输入数据，而是由于随机函数取值不佳。实际上，随机化快速排序得到理论最坏情况的可能性仅为1/(2^n）。所以随机化快速排序可以对于绝大多数输入数据达到O(nlogn）的期望时间复杂度。一位前辈做出了一个精辟的总结：“随机化快速排序可以满足一个人一辈子的人品需求。”

随机化快速排序的唯一缺点在于，一旦输入数据中有很多的相同数据，随机化的效果将直接减弱。对于极限情况，即对于n个相同的数排序，随机化快速排序的时间复杂度将毫无疑问的降低到O(n^2）。解决方法是用一种方法进行扫描，使没有交换的情况下主元保留在原位置。

平衡快排（Balanced Quicksort）：每次尽可能地选择一个能够代表中值的元素作为关键数据，然后遵循普通快排的原则进行比较、替换和递归。通常来说，选择这个数据的方法是取开头、结尾、中间3个数据，通过比较选出其中的中值。取这3个值的好处是在实际问题（例如信息学竞赛……）中，出现近似顺序数据或逆序数据的概率较大，此时中间数据必然成为中值，而也是事实上的近似中值。万一遇到正好中间大两边小（或反之）的数据，取的值都接近最值，那么由于至少能将两部分分开，实际效率也会有2倍左右的增加，而且利于将数据略微打乱，破坏退化的结构。

外部快排（External Quicksort）：与普通快排不同的是，关键数据是一段buffer，首先将之前和之后的M/2个元素读入buffer并对该buffer中的这些元素进行排序，然后从被排序数组的开头（或者结尾）读入下一个元素，假如这个元素小于buffer中最小的元素，把它写到最开头的空位上；假如这个元素大于buffer中最大的元素，则写到最后的空位上；否则把buffer中最大或者最小的元素写入数组，并把这个元素放在buffer里。保持最大值低于这些关键数据，最小值高于这些关键数据，从而避免对已经有序的中间的数据进行重排。完成后，数组的中间空位必然空出，把这个buffer写入数组中间空位。然后递归地对外部更小的部分，循环地对其他部分进行排序。

三路基数快排（Three-way Radix Quicksort，也称作Multikey Quicksort、Multi-key Quicksort）：结合了基数排序（radix sort，如一般的字符串比较排序就是基数排序）和快排的特点，是字符串排序中比较高效的算法。该算法被排序数组的元素具有一个特点，即multikey，如一个字符串，每个字母可以看作是一个key。算法每次在被排序数组中任意选择一个元素作为关键数据，首先仅考虑这个元素的第一个key（字母），然后把其他元素通过key的比较分成小于、等于、大于关键数据的三个部分。然后递归地基于这一个key位置对“小于”和“大于”部分进行排序，基于下一个key对“等于”部分进行排序。

### 实例

![](http://onnq25vz1.bkt.clouddn.com/kuaisu.png)