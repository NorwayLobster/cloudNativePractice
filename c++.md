<!--
 * @Author: your name
 * @Date: 2020-11-27 07:58:35
 * @LastEditTime: 2020-12-01 10:52:44
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /note/c++.md
-->
C++ STL 的 vector 容器在 clear() 之后不会释放内存，需要 swap(empty vector)，这是有意为之（C++11 里增加了 shrink_to_fit() 函数）。不要记成了所有 STL 容器都需要 swap(empty one) 来释放内存，事实上其他容器（map/set/list/deque）都只需要 clear() 就能释放内存。只有含 reserve()/capacity() 成员函数的容器才需要用 swap 来释放空间，而 C++ 里只有 vector 和 string 这两个符合条件。

作者：陈硕
链接：https://www.zhihu.com/question/22608820/answer/21968467
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

# 1. lambda表达式,作为匿名对象，会把捕获列表中的shHandle作为成员变量,而该handler对象中有该lambda表达式作为成员变量。
        其中捕获列表中获取shHandler,并不适用shHanlder，只是简单的捕获，目的使延长shHandler的生命期，防止异步回调时，shHandler已经析构。
# 2. UT的问题是：没有真正模拟处数据库的异步，导致很多，异步回调问题，没法在UT浮现，而在FT中爆出，增加开发成本。
# 3. lambda表达式，传参时传引用？异步回调时有问题？？？？？？？ 应该没问题，lib库中都是传的引用。
# 4.  coredump从container中导出的问题，及其实现原理:initContainer, empty_dir,....
# 5. gdb a.out core: 学习
# 5.1 gdb attach pid: 学习
# 6. 回调函数，1.同步的进程，一直阻塞，需要curl然后才能继续,执行回调函数（同步回调）; 2. 异步回调，访问数据库，数据库的返回时异步，数据返回时才执行刚才访问数据库时注册的函数。
# 7. pod中的各个container,之间的通信在pod外面是无法tcpdump抓包抓到的，需要进入pod里面，和各个container在同一网络环境才可以。