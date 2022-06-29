# Sequence Types - list, tuple, range

:::info
- **list(串列) :** 
串列：由零或多個元素組成的，以「,」逗號分隔，並且放在[]裡面。
語法：[ 元素1 , 元素2..... ]

- **range( ) :**
range：建立整數的串列可用range
語法: range(起始值,終止值, 間格值)

- **Tuple( 元組 ) ：**
Tuple:不能修改的List
優點：執行速度比list快，儲存在Tuple的資料比較安全
語法：( 元素1 , 元素2..... )

:::

## list(串列)

```python=
a_list = [ "a" , "b" , "c" ]

#取值
print ( 'frist' , a_list[ 0 ] )
print ( 'last' , a_list[ 2 ] )

```

>輸出:
frist a
last c

* ## list 基本指令

1. <font color = green > **串列重複** </font>
語法：list[ ]*n , 串列重複n次

```python=
a_list = [ "aa" , "bb" , "cc" ]
b_list = a_list * 2

#輸出
print ( b_list )

```

>輸出:
[ 'aa' , 'bb' , 'cc' , 'aa' , 'bb' , 'cc' ]

2. <font color = green > **切片取值1** </font>
語法：[ n , m ] 取出 index n ~ ( m - 1 )的元素

```python=
a_list = [ "aa" , "bb" , "cc" , "dd" , "ee" , "ff" ]

print( list ( ironman_list1 [ 2 : 5 ] ) )

#輸出
print ( b_list )

```

>輸出:
[ 'cc' , 'dd' , 'ee' ]

3. <font color = green > **切片取值2** </font>
語法：[ n , m , o ] 取出 index n ~ ( m - 1 ) 的元素，間隔為o

```python=
a_list = [ "aa" , "bb" , "cc" , "dd" , "ee" , "ff" ]

print( list ( ironman_list1 [ 1 : 4 : 2 ] ) )

#輸出
print ( b_list )

```

>輸出:
[ 'bb' , 'dd' ]

4. <font color = green>刪除元素</font>
語法：del

```python=
a_list = [ "aa" , "bb" , "cc" , "dd" , "ee" , "ff" ]
#以切片的方式刪除元素
del a_lisst[ 1 : 4 ]  #刪除索引值 1 ~ 3

#輸出
print ( b_list )

```

>輸出:
[ 'aa' , 'ee' , 'ff' ]

* ## list 進階指令

1.  <font color = green>串列預設函數</font>
    * len()：串列元素數目
    * min()：串列元素最小值
    * max()：串列元素最大值

2.  <font color = green>在串列中想取得某個元素</font>
    * index()：元素在串列中第一次出現的index
    * count()：元素在串列中出現的次數

3. <font color = green>在list中加入元素</font>
    * A.append(E)：在A串列中加入E元素
    * A.extend(B)：在A串列中加入B串列的元素
    * A.insert(B)：在A串列中加入B串列

:::spoiler
extend和insert雖然B同樣都是串列，但加入A串列的方式不一樣
:::

4. <font color = green>移除串列的元素</font>
    * pop()：取出串列中最後一個元素，並且移除元素
    * A.remove(E)：移除A串列中第一個出現E元素

5. <font color = green>其他串列函數操作</font>
    * reverse()：反轉串列的順序
    * sort()：將串列做排序

```python=
a_list = [ 1 , 3 , 3 , 4 , 5 , 6 ]

#輸出
#1.
print( len( a_list ) ) #a_list長度
print( min( a_list ) ) #a_list裡最小值
print( max( a_list ) ) #a_list裡最大值

#2.
print( a_list.index( 3 ) ) #元素3第一次出現的位置
print( a_list.count( 3 ) ) #元素在串列中出現的次數

#3.
a_list.append(8)
print( list( a_list ) ) #將8做為元素加在list最後

a_list.extend( [8,9] )
print( list( a_list ) ) #將[8,9]中的元素加在list最後

a_list.insert( 3 , 8 )
print( list( a_list ) ) #在index 3的位置加入元素8 

#4.
n = a_list.pop()
print( n ) #取出list最後一個元素並且移除

a_list.remove( 3 )
print( list( a_list ) ) #移除第一次出現3的元素

#5.
a_list.reverse()
print( list( a_list1 ) ) #反轉list順序

a_list1 = [6,2,1,5,7,4]
a_list1.sort()
print( list( a_list1 ) ) #將list從小到大排列

```

>輸出:
>>1.
>>>6
>>>1
>>>6
>
>>2.
>>>2
>>>2
>
>>3.
>>>[ 1 , 3 , 3 , 4 , 5 , 6 , 8 ]
>>>[ 1 , 3 , 3 , 4 , 5 , 6 , 8 , 8 , 9 ]
>>>[ 1 , 3 , 3 , 8 , 4 , 5 , 6 , 8 , 8 , 9 ]
>
>>4.
>>>9
>>>[ 1 , 3 , 8 , 4 , 5 , 6 , 8 , 8 ]
>
>>5.
>>>[ 8 , 8 , 6 , 5 , 4 , 8 , 3 , 1 ]
>>>[ 1 , 2 , 4 , 5 , 6 , 7 ]

## range( )

* <font color = green>如果只建立整數的串列可用range</font>
    * 語法: range( 起始值 ,終止值 , 間格值 )

```python=
a_list = range( 5 )
b_list = range( 3 , 8 )
c_list = range( 1 , 7 , 2 )

print( a_list )
print( b_list )
print( c_list )

```

>輸出:
>[ 0 , 1 , 2 , 3 , 4 ]
>[ 3 , 4 , 5 , 6 , 7 ]
>[ 0 , 2 , 4 , 6 ]

## Tuple( 元組 )：不能修改的List

```python=
a_tuple = ( "aa" , "bb" , "cc" )

print( 'frist' , a_tuple[0] )
print( 'last' , a_tuple[-1] )
```

>輸出:
>frist aa
>last cc

* <font color = green>如果 list 和 tuple 互相轉換</font>

```python=
#宣告
a_list = [ "a" , "b" , "c" ]
a_tuple = ( "d" , "e" , "f" )

#宣告轉換的 list、tuple
list_to_tuple = tuple( a_list )
tuple_to_list = list( a_tuple )

#輸出
print( list ( list_to_tuple ) )
print( list ( tuple_to_list ) )
```

>輸出:
>[ a , b , c ]
>[ d , e , f ]
