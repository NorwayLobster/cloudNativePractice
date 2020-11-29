<!--
 * @Author: your name
 * @Date: 2020-11-27 07:58:35
 * @LastEditTime: 2020-11-27 07:58:35
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /note/c++.md
-->
C++ STL 的 vector 容器在 clear() 之后不会释放内存，需要 swap(empty vector)，这是有意为之（C++11 里增加了 shrink_to_fit() 函数）。不要记成了所有 STL 容器都需要 swap(empty one) 来释放内存，事实上其他容器（map/set/list/deque）都只需要 clear() 就能释放内存。只有含 reserve()/capacity() 成员函数的容器才需要用 swap 来释放空间，而 C++ 里只有 vector 和 string 这两个符合条件。

作者：陈硕
链接：https://www.zhihu.com/question/22608820/answer/21968467
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。