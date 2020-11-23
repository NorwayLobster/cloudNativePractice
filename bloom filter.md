<!--
 * @Author: your name
 * @Date: 2020-11-22 23:15:20
 * @LastEditTime: 2020-11-22 23:19:11
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /note/bloom filter.md
-->
[bloom filter](https://www.cnblogs.com/liyulong1982/p/6013002.html)
[wiki](https://en.wikipedia.org/wiki/Bloom_filter)
# hash func selected:
    CRC32

    Instead of using k different hash functions, this implementation seeds the CRC32 hash with k different initial values (0, 1, ..., k-1). This may or may not give you a good distribution, it all depends on the data.

    Performance of the Bloom filter depends on a number of variables:

    size of the bit array
    size of the counter bucket
    number of hash functions