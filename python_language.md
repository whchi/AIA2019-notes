* list
```py
[a, b]
```
list[::3] => 每三個為一個區間跳耀
list[2:5] => 3th ~ 5th
list[:] => 0 ~ last
list[:-3] => 0 ~ last-3
list[-1] => last
* tuple
```py
(a, b)
```
tuple saves reference, list save value, so tuple is immutable
* set
```py
{a, b}
```
unordered, unique elements and immutable
union: set1 | set2
intersection: set1 & set2
symmetric difference: set1 - set2
* dict
```py
{'a': 'a', 'b': 'b'}
```
key->val pair
zip: iterator to tuple and return list
* enumerate
change iterator into  index-value pair
* List comprehension
a consice way to create list
```py
x = [y for y in range(10)]
# FizzBuzz
x = ['Fizz'*(not i % 3) + 'Bazz' * (not i % 5) or i for i in list(range(1, 51))]
# not 0 == 1 (True == True), only works in python3.*
```
* some practice
Q1: input 'test', output 'tset'
Q2: input 'string is' output 'gnirts si'
Q1sol1:
    str[::-1]
Q1sol2:
s = list(s)
l = 0
r = len(str) - 1
while r > l:
    swap(s[l], s[r])
    l++
    r--
return ''.join(s)
Q2sol:
s = list(s).split(' ')
for i in len(s):
    s[i] = reverse(s[i])
return ' '.join(s)

* [generator](https://stackoverflow.com/questions/231767/what-does-the-yield-keyword-do?rq=1)
回傳 yield 當下的狀態後繼續執行\
不把值存在memory裡面\
建立 iteratble 的一種方式\
The difference is that, while a return statement terminates a function entirely, yield statement pauses the function saving all its states and later continues from there on successive calls.
* list extend vs append
extend: 展開舊的 list 之後再把值塞進去,extend 參數只能是 iterable
