---
title: "Algorithm"
date: 2026-08-12
tags:
  - Data Structure
  - Algorithm
---

# 1 Basics of C++

## 1.1 Standard Code Framework

```cpp
#include <bits/stdc++.h>

using namespace std;

int main()
{

  return 0;
}
```

## 1.2 Input and Output

### 1.2.1 Basic Input : cin

Enter an integer

```cpp
int n;

cin >> n;

cout << n;
```

Enter multiple variables

```cpp
int a,b;

cin >> a >> b;

cout << a+b;
```

Enter multiple numbers in one line

```cpp
int n;

cin >> n;

for(int i = 0; i < n; i++)
{
  cin >> a[i];
}
```

### 1.2.2 Basic Output : cout

Single output

```cpp
cout << "hello" << endl;

cout << "hello\n";
```

Multiple outputs

```cpp
int a = 10;

cout << "value=" << a;
```

### 1.2.3 Speed up Input and Output

```cpp
int main()
{
  ios::sync_with_stdio(false);
  
  cin.tie(nullptr);
}
```

## 1.3 Data Type

### 1.3.1 Integer Type : int

Range : $-2^{31} \sim 2^{31} - 1$​

```cpp
int a = 100;
```

### 1.3.2 Long Integer Type : long long

Range : $-2^{63} \sim 2^{63} - 1$​

```cpp
long long sum = 10000000000LL*10;
```

### 1.3.3 Floating-point Type

Low precision : float

```cpp
float x = 3.14;
```

High precision : double

```cpp
double x = 3.1415926;
```

### 1.3.4 Character Type : char

A character

```cpp
char c = 'a';
```

String

```cpp
char s[] = "hello";
```

### 1.3.5 Boolean Type : bool

```cpp
bool flag = true;
```

### 1.3.6 Constant : const

```cpp
const int MAX = 1000;
```

## 1.4 Operator

### 1.4.1 Arithmetic Operations

| **Operator** | **Meaning**    |
| ------------ | -------------- |
| +            | Addition       |
| -            | Subtraction    |
| \*           | Multiplication |
| /            | Division       |
| %            | Modulo         |

### 1.4.2 Comparison Operations

| **Operator** | **Meaning**              |
| ------------ | ------------------------ |
| >            | Greater than             |
| \<           | Less than                |
| >=           | Greater‑than or equal to |
| \<=          | Less‑than or equal to    |
| ==           | Equal to                 |
| !=           | Not equal to             |

### 1.4.3 Logical Operations

| **Operator** | **Meaning** |
| ------------ | ----------- |
| &&           | and         |
| \|\|         | or          |
| !            | not         |

## 1.5 Conditional Statement

### 1.5.1 if

```cpp
if(x>0)
{

}
else if(x==0)
{

}
else
{

}
```

### 1.5.2 switch

```cpp
switch(x)
{

case 1:
  cout << "one";
  break;

case 2:
  cout << "two";
  break;
  
default:
  break;

}
```

## 1.6 Loop Statement

### 1.6.1 for

```cpp
for(int i = 0; i < n; i++)
{

}
```

### 1.6.2 while

```cpp
while(condition)
{

}
```

### 1.6.3 do while

```cpp
do
{

}
while(condition);
```

## 1.7 Array

One-dimensional array

```cpp
int a[5] = {1,2,3,4,5}
```

Multidimensional array

```cpp
int a[100][100];
```

## 1.8 String

```cpp
string s = "hello";
```

## 1.9 Parameter Passing

### 1.9.1 Pass-by-value

Modifications will not affect the original variable.

```cpp
void func(int x)
{

}
```

### 1.9.2 Pass-by-reference

Avoid copying to save time and memory.

```cpp
void change(int &x)
{
  x++;
}
```

## 1.10 Pointer

Address

```cpp
int a = 10;

cout << &a;
```

Pointer

```cpp
int *p = &a;
```

## 1.11 Memory

### 1.11.1 Stack

Automatic management

```cpp
int a;
```

### 1.11.2 Heap

Dynamic application and release

```cpp
int *p = new int;

delete p;
```

## 1.12 Tips

### 1.12.1 Common Functions

Maximum

```cpp
int a = 10;
int b = 20;
int c = 30;

cout << max(a,b) << max({a,b,c});
```

Minimum

```cpp
int a = 10;
int b = 20;
int c = 30;

cout << min(a,b) << min({a,b,c});
```

Swap variables

```cpp
swap(a,b)
```

Absolute value

```cpp
int x = abs(-10);                     // int

long long y = llabs(-100000000000LL)  // long long

double z = fabs(-3.1415)              // double
```

Get the length of the array

```cpp
int a[] = {1,2,3,4)

int n = sizeof(a) / sizeof(a[0])
```

> When passing parameters to a function, a is not an array but a pointer.
>
> ```cpp
> void func(int a[])
> {
>   cout << sizeof(a);  // the byte size of the pointer, not the size of the entire array
> }
> ```

Mathematical function

| **Function** | **Meaning**    | **Example**               |
| ------------ | -------------- | ------------------------- |
| sqrt()       | Square‑root    | `double x = sqrt(16);`    |
| pow(a,b)     | Exponentiation | `double x = pow(2,3);`    |
| ceil()       | Round‑up       | `double x = ceil(3.2);`   |
| floor()      | Round‑down     | `double x = floor(3.9);`  |
| round()      | Rounding       | `double x = round(3.6);`  |
| log()        | Natural‑log    | `double x = log(2.718);`  |
| sin()        | Sine           | `double x = sin(1.5708);` |
| cos()        | Cosine         | `double x = cos(0);`      |
| tan()        | Tangent        | `double x = tan(0.7854);` |

Reverse

```cpp
reverse(a,a+n);              // array

reverse(v.begin(),v.end());  // vector

reverse(s.begin(),s.end());  // string
```

Sort

```cpp
// ascending

sort(a,a+n);              // array

sort(v.begin(),v.end());  // vector

// descending

sort(a,a+n,greater<int>());

sort(v.begin(),v.end(),greater<int>());
```

Unique : remove only adjacent duplicates.

```cpp
sort(v.begin(),v.end());

v.erase(unique(v.begin(),v.end()),v.end());
```

Fill Initialize

```cpp
// one-dimensional array

int a[100];

fill(a,a+100,0);

// two‑dimensional array

int a[100][100];

fill(&a[0][0],&a[0][0]+10000,0);
```

Binary search for the first position where the element is greater than or equal to x.

```cpp
auto it = lower_bound(v.begin(),v.end(),x);

int pos = it - v.begin();  // distance
```

Binary search for the first position where the element is greater than x.

```cpp
auto it = upper_bound(v.begin(),v.end(),x);

int pos = it - v.begin();  // distance
```

### 1.12.2 Common Numerical Tips

Check odd‑even : bitwise operations are faster than modulo operations.

```cpp
if(n & 1)
{

}
```

Check for multiples

```cpp
if(n % 3 == 0)
{

}
```

Greatest common divisor

```cpp
gcd(a,b)
```

Least common multiple

```cpp
lcm(a,b)

a / gcd(a,b) * b  // prevent overflow
```

Maximum value of the data type

```cpp
int ans = INT_MAX;

long long ans = LLONG_MAX;
```

Minimum value of the data type

```cpp
int ans =  INT_MIN;

long long ans = LLONG_MIN;
```

### 1.12.3 Bitwise Operation

Left shift : equivalent to multiplying by 2

```cpp
1 << n
```

Right shift : equivalent to dividing by 2

```cpp
8 >> n
```

Check the n‑th bit

```cpp
if((n >> k) & 1)
{

}
```

Lowbit : get the decimal value of the least significant 1 bit

```cpp
x & (-x)
```

Count the number of 1

```cpp
int x;

__builtin_popcount(x)

long long y;

__builtin_popcountll(y)
```

## 1.13 Standard Template Library

### 1.13.1 Vector

Definition

```cpp
vector<int> v;  // empty vector

vector<int> v(10);  // specified size

vector<int> v(10,5)  // specify the initial value
```

Function

```cpp
// add element to the end
v.push_back(10);

// delete the last element
v.pop_back();

// get container size
int n = v.size();

// check if the container is empty
if(v.empty())
{

}

// clear all elements
v.clear();

// access the first element
v.front();

// access the last element
v.back();

// traverse the container
for(int i = 0; i < v.size(); i++)
{
  cout << v[i];
}

for(int x : v)
{
  cout << x;
}

for(int &x : v)
{
  x++;
}
```

Tips

```cpp
// sort
sort(v.begin(),v.end());

// reverse
reverse(v.begin(),v.end());

// delete the i‑th element
v.erase(v.begin()+i);

// delete elements in range: left‑closed right‑open
v.erase(v.begin()+l,v.begin()+r);
```

### 1.13.2 String

Definition

```cpp
string s;

string s = "hello";
```

Function

```cpp
// get container size
s.size();

s.length();

// access the i‑th character
s[i];

// add element to the end
s.push_back('a');

// delete the last element
s.pop_back();

// intercept substring
substr(start,length);

// search, returns string::npos when not found
s.find("abc");

// delete elements in range
s.erase(start,length);

// insert "abc" before the i‑th element
s.insert(i,"abc");

// convert string to integer
stoi(s);

// convert number to string
to_string(x);
```

### 1.13.3 Unordered\_map

Definition

```cpp
unordered_map<int,int> mp;
```

Tips

```cpp
// add element
mp[key] = value;

// modify value
mp[x]++;

// search
if(mp.count(x))
{

}

auto it = mp.find(x);

if(it != mp.end())
{

}

// traverse
for(auto p:mp)
{
  cout << p.first;
  cout << p.second;
}

// delete element
mp.erase(key);
```

### 1.13.4 Map

| **​**                    | **map**        | **unordered\_map** |
| ------------------------ | -------------- | ------------------ |
| **underlying structure** | red‑black tree | hash table         |
| **order**                | ordered        | unordered          |
| **time complexity**      | O(logn)        | O(1)               |

Definition

```cpp
map<int,int> mp;
```

### 1.13.5 Unordered\_set

Definition

```cpp
unordered_set<int> s;
```

Function

```cpp
// add element
s.insert(10);

// search
if(s.count(10))
{

}

// delete element
s.erase(10);

// get container size
s.size();

// traverse
for(auto x:s)
{

}
```

### 1.13.6 Set

Definition

```cpp
set<int> s;
```

Function

```cpp
// add element
s.insert(10);

// search for element
s.find(x);

// find the first element greater than or equal to x
s.lower_bound(x);

// find the first element greater than x
s.upper_bound(x);

// delete element
s.erase(10);

// traverse
for(auto x:s)
{

}
```

### 1.13.7 Stack : first in last out

Definition

```cpp
stack<int> st;
```

Function

```cpp
// push element onto stack
st.push(x);

// pop the top‑most element
st.pop();

// access top element
st.top();

// check if empty
st.empty();

// get container size
st.size();
```

### 1.13.8 queue : first in first out

Definition

```cpp
queue<int> q;
```

Function

```cpp
// add element to queue
q.push(x);

// remove front element
q.pop();

// access front element
q.front();

// access back element
q.back();

// check if empty
q.empty();
```

### 1.13.9 deque

Definition

```cpp
deque<int> dq;
```

Function

```cpp
// add element to the front
dq.push_front(x);

// add element to the back
dq.push_back(x);

// remove front element
dq.pop_front();

// remove back element
dq.pop_back();
```

### 1.13.10 priority\_queue

Definition

```cpp
// max‑heap
priority_queue<int> q;

// min‑heap
priority_queue<int,vector<int>,greater<int>> q;
```

Function

```cpp
// add element to the heap
q.push(x);

// access top‑heap element
q.top();

// delete the top‑heap element
q.pop();
```

### 1.13.11 pair

Definition

```cpp
pair<int,int> p;
```

Tips

```cpp
// initialize
pair<int,int> p = {1,2};

// access the first data
p.first;

// access the second data
p.second;

// sort: compare first, then second
vector<pair<int,int>> v;

sort(v.begin(),v.end());
```

### 1.13.12 tuple

Definition

```cpp
tuple<int,int,int> t;
```

Function

```cpp
// read the first element of the tuple
get<0>(t);
```

### 1.13.13 Iterator

Definition

```cpp
vector<int>::iterator it;
```

Tips

```cpp
// traverse
for(auto it = v.begin(); it!=v.end(); it++)
{
    cout << *it;
}
```

### 1.13.14 Algorithm

Max\_element

```cpp
auto it = max_element(v.begin(),v.end());

// get the value
*it
```

Min\_element

```cpp
auto it = min_element(v.begin(),v.end());
```

Count

```cpp
count(v.begin(),v.end(),x);
```

Binary Search

```cpp
binary_search(v.begin(),v.end(),x);
```

Lower Bound : the first element greater than or equal to x

```cpp
lower_bound(v.begin(),v.end(),x);
```

Upper Bound : the first element greater than x

```cpp
upper_bound(v.begin(),v.end(),x);
```

# 2 Data Structure

## 2.1 Array

### 2.1.1 双指针

**适用场景：**

- 有序数组
- 子数组问题
- 快慢移动
- 两段收缩

**常见形式：**

1. **左右指针**

   - 模板

     ```c++
     int left = 0;
     int right = nums.size()-1;
     
     while(left < right)
     {
         if(condition)
             left++;
         else
             right--;
     }
     ```

   - 典型题目：
     - 两数之和
     - 三数之和
     - 盛最多水的容器
     - 删除有序数组重复元素
