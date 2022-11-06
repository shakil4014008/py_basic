# py_basic

```py
# without using any module
# s = "restaurant"
# mydict = {}
# for ch in s:
#   mydict[ch] = mydict.get(ch,0)+1
# print(mydict)

# by using collections module
# from collections import defaultdict
# s = "restaurant"
# mydict = defaultdict(int)
# for ch in s:
#   mydict[ch] +=  1
# print(mydict)

"""
input: nums = [10,10,22,13,45]
output:{
10: [0,1],
22: [2],
13: [3],
45: [4]
}
"""
# nums = [10,10,22,13,45]
# mydict = {}
# for i,num in enumerate(nums):
#   mydict[num] = mydict.get(num, []) + [i]
# print(mydict)
# with 
# from collections import defaultdict
# nums = [10,10,22,13,45]
# mydict = defaultdict(list)
# for i,num in enumerate(nums):
#   mydict[num] += [i]
# print(mydict)
# from collections import defaultdict
# from collections import Counter
# s = "Mohammed"
# c = Counter(s)
# print(c)
# mydict = defaultdict(int)
# for ch in s:
#   mydict[ch]  += 1
# print(mydict)


# a = a + 1 => a += 1
# a = a - 1 => a -= 1
# a = a * 2 => a *= 2
# a = a / 3 => a /= 3
# a = a//3 => a //= 3


x = 1
y = 1

n = 2
print([[i, j]
       for i in range(x + 1)
       for j in range(y + 1)
            if i + j != n])
            
            
Python 3.10.7 (v3.10.7:6cc6b13308, Sep  5 2022, 14:02:52) [Clang 13.0.0 (clang-1300.0.29.30)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
mydict = {"key1": "value1", "key2":"value2"}
"key1" in mydict
True
"key2" in mydict
True
"key3" in mydict
False
s1 = set()
s1
set()
s1.add(4)
s1
{4}
s1.add(5)
s1
{4, 5}
s1.add(7)
s1
{4, 5, 7}
s1.add(4)
s1
{4, 5, 7}
# unordered collection of unique elements
s1.add(100)
s1
{100, 4, 5, 7}
s1.add(110)
s1
{100, 4, 5, 7, 110}
100 in s1
True
10 in s1
False
11 in s1
False
120 in s1
False
len(s1)
5
s2 = set({11, 21, 32})
s2
{32, 11, 21}
s2.remove(11)
s2
{32, 21}
s2.remove(32)
s2
{21}
s2.remove(21)
s2
set()
s2.remove(33)
Traceback (most recent call last):
  File "<pyshell#32>", line 1, in <module>
    s2.remove(33)
KeyError: 33
s1
{100, 4, 5, 7, 110}
s1.remove(11)
Traceback (most recent call last):
  File "<pyshell#34>", line 1, in <module>
    s1.remove(11)
KeyError: 11
mydict
{'key1': 'value1', 'key2': 'value2'}
mydict["key1"]
'value1'
mydict["key3"]
Traceback (most recent call last):
  File "<pyshell#37>", line 1, in <module>
    mydict["key3"]
KeyError: 'key3'
mydict.get("key3", 0)
0
s1
{100, 4, 5, 7, 110}
s1.pop()
100
s1
{4, 5, 7, 110}
s1.pop()
4
s1
{5, 7, 110}
s1
{5, 7, 110}
s2
set()
s2.add(7)
s2.add(10)
s2.add(11)
s2
{7, 10, 11}
s1
{5, 7, 110}
>>> s1.intersection(s2)
{7}
>>> s1.union(s2)
{5, 7, 10, 11, 110}
>>> s1 + s2
Traceback (most recent call last):
  File "<pyshell#53>", line 1, in <module>
    s1 + s2
TypeError: unsupported operand type(s) for +: 'set' and 'set'
>>> s3 = set()
>>> for x in s1:
...     s3.add(x)
... 
...     
>>> for x in s2:
...     s3.add(x)
... 
...     
>>> s3
{5, 7, 10, 11, 110}
>>> s4 = set()
>>> for x in s1:
...     if x in s2:
...         s4.add(x)
... 
...         
s4
{7}
dir(s4)
['__and__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__iand__', '__init__', '__init_subclass__', '__ior__', '__isub__', '__iter__', '__ixor__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__or__', '__rand__', '__reduce__', '__reduce_ex__', '__repr__', '__ror__', '__rsub__', '__rxor__', '__setattr__', '__sizeof__', '__str__', '__sub__', '__subclasshook__', '__xor__', 'add', 'clear', 'copy', 'difference', 'difference_update', 'discard', 'intersection', 'intersection_update', 'isdisjoint', 'issubset', 'issuperset', 'pop', 'remove', 'symmetric_difference', 'symmetric_difference_update', 'union', 'update']
# list, tuple, dict, set
for i in range(10):
    print(i)

    
0
1
2
3
4
5
6
7
8
9
range(10)
range(0, 10)
for i in range(10,20):
    print(i)

    
10
11
12
13
14
15
16
17
18
19
for i in range(10):
    print(10)

    
10
10
10
10
10
10
10
10
10
10
for i in range(10):
    print(i)

    
0
1
2
3
4
5
6
7
8
9
fruits = ["orange", "banana", "cherry"]
n = len(fruits)
for i in range(n):
    print(fruits[i])

    
orange
banana
cherry
for fruit in fruits:
    print(fruit)

    
orange
banana
cherry
for index, fruit in enumerate(fruits):
    print(index, fruit)

    
0 orange
1 banana
2 cherry
n = 3
def pyramid(n):
    for i in range(n):
        spaces = n - i
        stars = i
        print(" "*spaces + "*"*stars + "*" + "*"*stars + " "*spaces)

        

pyrmaid(2)
Traceback (most recent call last):
  File "<pyshell#105>", line 1, in <module>
    pyrmaid(2)
NameError: name 'pyrmaid' is not defined. Did you mean: 'pyramid'?
pyramid(2)
  *  
 *** 
pyrmaid(3)
Traceback (most recent call last):
  File "<pyshell#107>", line 1, in <module>
    pyrmaid(3)
NameError: name 'pyrmaid' is not defined. Did you mean: 'pyramid'?
pyramid(3)
   *   
  ***  
 ***** 
pyramid(5)
     *     
    ***    
   *****   
  *******  
 ********* 
pyramid(6)
      *      
     ***     
    *****    
   *******   
  *********  
 *********** 
"mohammed" * 2
'mohammedmohammed'
"akhil" * 3
'akhilakhilakhil'
"*" * 3
'***'
" " * 4
'    '
"*" * 10
'**********'


```
