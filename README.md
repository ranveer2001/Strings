**PYTHON COMPLETE MASTERCLASS FOR BEGINNERS**


**STRINGS

A string in Python is a sequence of characters. Strings are immutable and hence once defined, the content cannont be modified/changed in any way.
Example : welcome = : "Hello Python"

Single quotes and Double quotes give the same result while entering a string.
Example : my_string = ' abcd ' 
      >>> my_string
      >>> ' abcd '
        : my_string = " abcd "
      >>> my_string
      >>> ' abcd '
\n is a new line character

The first element of any sequence when counting from left to right has index 0, second element has index 1 and so on..
Example : string1 = Ranveer Bhalla
          string1[0] = R
          string1[3] = v
          string1[7] = ' ' (spaces are also counted as characters)
          string1[-1] = a  (when negative index number, count from right to left)
          string1[-3] = l
To find the number of characters or length of the sequence use the 'len' function.
Example : len(string1)
      >>> 14

Methods of indexes :-
Example : a = Ranveer Bhalla
          a.index("e") (finds the index number of the first 'e')
      >>> 4
          a.count("e") (counts the number of times 'e' is present)
      >>> 2
          a.find("veer") 
      >>> 3            (counts from the first letter that is 'v' in this case)
          a.find("xyz")
      >>> -1           (returns -1 if cannot find the value)
          a.lower()
      >>> 'ranveer bhalla'
          a.upper()
      >>> 'RANVEER BHALLA'
          a.startswith("R")
      >>> TRUE
          a.endswith("p")
      >>> FALSE
          b = "   Ranveer Bhalla   "
          b.strip()
       >>> 'Ranveer Bhalla'
          c = "$$$Ranveer Bhalla$$$"
          c.strip("$")
       >>> 'Ranveer Bhalla'
          b = "   Ranveer Bhalla   "
          b.replace(" ", "")
       >>> 'Ranveer Bhalla'
          d = "apple,orange,banana,kiwi"
          d.split(",")
        >>> ['apple', 'orange', 'banana', 'kiwi']
          a = "Ranveer bhalla"
          "_".join(a)
        >>> 'R_a_n_v_e_e_r_ _B_h_a_l_l_a'
      
 Unifying 2 strings :-
 Example : x = "Ranveer"
           y = " Bhalla"
           x + y
       >>> "Ranveer Bhalla"
           x * 3
       >>> "RanveerRanveerRanveer"
String formatting :-
Example : "Cisco model: %s, %d WAN slots, IOS %.1f" % ("7200XR", 8, 15.4) 
    >>> 'Cisco model: 7200XR, 8 WAN slots, IOS 15.4'
(%s = string , %d = digit, %f = floating operator)
%s is a placeholder for string
%d follows same logic but for number instead of a string
%f refers to a decimal point number
** %.1f gives one decimal place after the number
   %.2f gives 2 decimal places
   %.f rounds to nearest whole number
  
Example : "Cisco model: {}, {} WAN slots, IOS {}".format("7200XR", 8, 15.4) (replace old formatting operator with curly braces and .format after the braces)
      >>> 'Cisco model: 7200XR, 8 WAN slots, IOS 15.4' (same result as before but different formatting method)
          "Cisco model: {0}, {1} WAN slots, IOS {2}".format("7200XR", 8, 15.4)
          'Cisco model: 7200XR, 8 WAN slots, IOS 15.4' (again same result as the indexing is done right)
          
Formatting using f-strings :-
Example : model = "7200XR"
          slots = 9
          ios = 15.4
      >>> f"Cisco model: {model}, {slots} WAN slots, IOS {ios}"
          'Cisco model: 7200XR, 8 WAN slots, IOS 15.4'
          f"Cisco model: {model.lower()}, {slots * 2} WAN slots, IOS {ios}"
          'Cisco model: 7200xr, 16 WAN slots, IOS 15.4'
     
String slice :-
Example : string1 = "O E2 10.110.8.9 [160/5] via 10.119.254.6, 0:01:00, Ethernet2"
          string1[5: 15] (count from 5 to 15 and dont include the 15th character)
          '10.110.8.9'
          string1[5: ] (from 5th to all characters)
          '10.110.8.9 [160/5] via 10.119.254.6, 0:01:00, Ethernet2'
          string1[ :10] (all characters till 10th)
          'O E2 10.11'
          string1[:]
          'O E2 10.110.8.9 [160/5] via 10.119.254.6, 0:01:00, Ethernet2'
          string1[-1] (last character)
          '2'
          string1[-9:-1] (last 9 characters but dont include the last one)
          'Ethernet'
          string1[-5:] (last 5 characters)
          'rnet2'
          string1[:-5] (all charcters till 5th last)
          'O E2 10.110.8.9 [160/5] via 10.119.254.6, 0:01:00, Ethe'
          string1[::2] (every second value will be neglected)
          'OE 01089[6/]va1.1.5.,00:0, tent' 
          string1[::-1] (write the characters in reverse order)
          '2tenrehtE ,00:10:0 ,6.452.911.01 aiv [5/061] 9.8.011.01'

String slicing using a step :-
Example : mystring = "0123456789"
          mystring[start:stop:step]
          mystring[::2]
          '02468'
          mystring[1::2]
          '13579'
          mystring[1:7:2]
          '135' (will not include the characters on which we need to stop, here it is 7)
          



**NUMBERS AND BOOLEANS

num1 = 10
num2 = 2.5
type(num1)
<class,'int'>
type(num2)
<class,'float'>
2 - 1
1
5 / 2
2.5
5 // 2 (divide to nearest whole number)
2
4 * 2
8
4 ** 2 (** is power function where 4 is base and 2 power)
16
5 == 5 (equalities)
True
5 != 4 (not equal to)
True
-> Priority while solving an equation :-
1) raising to a power
2) multiplication, divison, remainder, mosulus
3) Addition, subtraction
Example : 100 - 5 ** 2 / 5 * 2 (when same priority go from left to right)
          100 - 25 / 5 * 2
          100 - 5 * 2
          100 - 10
          90
    
int(1.7)
1
float(2)
2.0
abs(5)
5
abs(-5)
5
max(1,2)
2
min(1,2)
1
pow(3,2)
9

1 == 1
True
1 == 2
False
-> Logical expression :-
1) and - both expressions should be true
2) or - one of the expression should be true
3) not - negating an expression

Example : (1 == 1) and (2 == 2)
          T and T
          T
          (1 == 2) and (3 == 2)
          F and F
          F
          1 == 1 or 2 == 2
          T or T
          T
          1 == 1 or 2 ==3
          T or F
          T
          not(1 == 1)
          not(T)
          F
          not(1 == 2)
          not(F)
          T
bool functions evaluate functions as true or false
bool(None)
False
bool(0)
False
bool(' ')
False
bool(1)
True
bool(2.2)
True
bool([3])
True


          

**LISTS

Sequence of elements inclosed by [] brackets.
list1 = []
type(list1)
<class,'list'>
list 1 = ["apple", "kiwi", "orange", 2, 5.5, -8]
len(list1)
6
list1[0]
apple
list1[-1]
-8
list 1 = ["apple", "kiwi", "orange", 2, 5.5, -8]
list1[2] = "banana
list1
list1 = ["apple", "kiwi", "banana", 2, 5.5, -8]

list2 = [ 3, 5, -8]
min(list2)
-8
max(list2)
5

list 1 = ["apple", "kiwi", "orange", 2, 5.5, -8]
list1.append(100)
list1
["apple", "kiwi", "orange", 2, 5.5, -8, 100]
del list1[4]
list1
list 1 = ["apple", "kiwi", "orange", 2, -8, 100]
list1.pop(0)
list1
["kiwi", "orange", 2, -8, 100]
list1.remove("orange")
list1
["kiwi", 2, -8, 100]
list1.insert(2, "mango")
list1
["kiwi", 2, mango, -8, 100]
list2 = [2, 22, 222]
list1.extend(list2)
list1
["kiwi", 2, mango, -8, 100, 2, 22, 222]
list3 = [3, 5, 7, 29, 1, 2]
list3.sort() (sort in ascending order)
list3
[1, 2, 3, 5, 7, 29]
list3.reverse() (sort in descending order but only after first sorting in ascending order)
[29,7,5,3,2,1]

list4 = [1, 2, 3, 'a', 'b', 'c']
list4[0:3]
[1,2,3]
and so on..




**SETS

They are unordered collection of unique elements. They are basically lists without any duplicate elements.
list4 = [1,2,3,4,2,3,5]
set(list4)
{1, 2, 3, 4, 5}
set1 = set([11,12,13,14,15,15,15,11])
set1
{11, 12, 13, 14, 15}
type(set1)
<class,'set'>
len(set1)
5
11 in set1
True
100 in set1
False
set1.add(16)
set1
{11, 12, 13, 14, 15, 16}
set1.remove(11)
set1
{12, 13, 14, 15, 16}

set1 = {1, 2, 3, 4}
set2 = {3, 5, 8}
set1.intersection(set2)
{3}
set1.difference(set2)
{1, 2, 4}
set1.union(set2)
{1, 2, 3, 4, 5, 8}
set1.pop()
1
set1
{2, 3, 4}
set1.clear()
set1
>> 

list1 = [1, 2, 3, 4]
list2 = [3, 4, 7]
fs1 = frozenset(list1)
fs2 = frozenset(list2)

fs1
frozenset({1, 2, 3, 4})
fs2
frozenset({3, 4, 7})
type(fs1)
<class,'frozenset'>
*You cannot add, subtract, multiply, divide anything in the frozenset




**TUPLES

Tuples are ordered collection of non-unique elements.
my_tuple = ()
type(my_tuple)
<class,'tuple'>
my_tuple = 9
typle(my_tuple)
<class,'int'>
my_tuple = (9, )
type(my_tuple)
<class,'tuple'>

tuple1 = ("Mango", "Banana", "apple")
(2, 3, 5) = tuple1
"Mango"
2
"Banana"
3
"apple"
5

-> Tuples v/s lists
1) tuples are immutable; lists are mutable
2) tuples have fixed length; lists have variable length
3) tuples (); lists []

tuple2 = (1, 2, 3, 4)
len(tuple2)
4
max(tuple2)
4
tuple2 + (5, 6, 7)
tuple2
(1, 2, 3, 4, 5, 6, 7)
tuple2 * 2
(1, 2, 3, 4, 1, 2, 3, 4)
del tuple2
>>




**RANGES

print range(10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]     * Don't include 10
print range(5,10)
[5, 6, 7, 8, 9]

r = range(10)
r
range(0,10)
type(r)
<class,'range'>
list(r)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
r[0]
0
r[-1]
9
7 in r
True
22 in r
false
r.index(4)
4
list(r)[2:5]
[2, 3, 4]




**DICTIONARIES

dict1 = {}
type(dict1)
<class,'dict'>
dict1 = {"apple": "2", "mango": "3", "banana": "4"}
dict1["apple"]
'2'
dict1['mango']
'3'
dict1["Kiwi"] = "5"
dict1
{"apple": "2", "mango": "3", "banana": "4", "Kiwi": "5"}
dict1.keys()
dict_keys(['apple', 'mango', 'banana', 'kiwi'])
dict.values()
dict_values(['2', '3', '4', '5'])
dict1.items()
dict_items([('apple', '2'), ('mango', '3'), ('banana', '4'), ('kiwi', '5')])

-> Conversion between data types :-

-> int. or float to string
num = 2
f = 2.5
type(num)
<class,'num'>
type(f)
<class,'float'>

num2 = str(num)
num2
2
type(num2)
<class,'str'>

f2 = str(f)
f2
2.5
type(f2)
<class,'str'>

-> string to integer
str = "5"
type(str)
<class,'str'>
str1 = "5"
type(str1)
<class,'str'>
int1 = int(str1)
int1
5
type(int1)
<class,'int'>

-> string to float
f3 = float(str1)
type(f3)
<class,'float'>

-> integer to float function
num1 = 2
num1
2
type(num1)
<class,'int'>
f = float(num1)
type(f)
<class,'float'>
f
2.0

-> float to integer
f1 = int(f)
f1
2
type(f1)
<class,'int'>

-> tuple to list
tup1 = (1, 2, 3)
type(tup1)
<class,'tuple'>
list1 = list(tup1)
type(list1)
<class,'list'>

-> list to tuple
list1
[1, 2, 3]
tup = tuple(list1)
tup
(1,2,3)

-> list to set
list1
[1, 2, 3]

list1 = set(list1)
type(set1)
<class,'set'>

-> num to binary
num = 10
num_bin = bin(num)
num_bin
'0b1010'

-> num to hexadecimal
num = 10
num_hex = hex(num)
num_hex
'0xa'

-> binary and hex to decimal notation
bin_to_num = int(num_bin, 2)
bin_to_num
10

hex_to_num = int(num_hex, 16)
hex_to_num
10




**TYPES OF ERRORS IN PYTHON

1) Syntax Error
2) Exceptions



**FUNCTIONS

-> def function_name ():

def my_first_function(x):   (Here x is the parameter, used while defining a function)
    "This is my first function!"
    print(x)
     
    my_first_function("Hello Python!"). (Here Hello Python is the arguement, used while calling a function)
>>> Hello Python

**NAMESPACES

1) Built-in Namespaces -> print(list(range(10)))
                          [0,1,2,3,4,5,6,7,8,9]
                       
2) Global Namespaces -> my_var = 10
                        print(my_var)
                        10
                        
3) local Namespaces -> def my_var_func() :
                            my_var = 10
                            print(my_var)
                         
                       my_var_func()
                       my_var = 20
                       print(my_var * 20)
                       10
                       200
                       



**IMPORTING

from my_module import my_var
print("this is my app")
print(my_var)
my_function()




**OPEN A FILE

myfile = open("D:\\routers.txt", 'r')

r -> reading
w -> writing
a -> appending
b -> binary
x -> exclusive creation

-> Additional way of avoiding unicode error
f = open(r"D:\Users\teodo\file1.py",'w')
r here is **raw string literal
\U and \t are treated as normal characters due to the use of r which avoids the unicode error.

Unicode Error : Typical error on Windows because the default user directory is C:\user\<your_user> , so when you want to use this path as an string parameter into a Python function, you get a Unicode error, just because the \u is a Unicode escape. Any character not numeric after this produces an error.

Using w+ , will open a file for reading and writing at the same time and if the file does not exist, it will create it.

-> For writing and then close a file on it's own :
with open("newfile.txt",'w') as f:
     f.write("Hello Python!!!")
     
f.closed
True
     



**REGULAR EXPRESSIONS

A regular expression is represented by a special syntax that helps you match and find a pattern.
Example **in the python code under regex-search( ) heading.

In regular expression :
1) . represents any character except a new line character.
2) + represents that previous expression may repeat one or more times.
3) * represents that previous expression may repeat zero or more times.
4) ? represnts matching as minimal expressions as possible.
5) \d represents any decimal digit.
6) \w represnts letter (a-z, A-Z), numbers(0-9), underscore(_).
7) \s represents any white space character.
8) {2,} this means that python should expect 2 or more occurances of the pattern preeceding the curly braces.
9)    + or space before a plus sign after the parenthesis means that we want to indicate to python that we intend to match a group until a space is encountered.
10) \. means character escaping.
11) \D represents any non-digit character in the string. (*D+/S+/W+ for one or more repititions.)
12) \S represents all non-white space characters.
13) \W represents all non-word charcaters.(no letter, numbers, underscore)
14) [a-z] finds all lower case characters in the string.
15) [^a] represents all characters in the string except a.
16) A|B represents two different patterns tried from left to right. When one pattern matches inside the string, the other is no longer in use.




**Lambda function

lambda arg1, arg2 ..., ..., arg n: an expression using the arguements

**Iterators

Iterator is an object which allows a programmer to go through all the elements of a collection sequence regardless of its specific implementation.
iter()

Generator is a special routine that can be used to control the iteration behaviour of a loop.
It yields the value one at a time, unlike function.

1) chain() takes several sequences as arguements and chains them together.
2) count() returns an iterator that generates consecutive integers until you stop it,
3) cycle() returns an iterator that simply repeats the value given as an arguement infinitely.




**2D NUMPY ARRAYS

np_2d = np.array([[1.73, 1.68, 1.71, 1.89, 1.79], [56.5, 76.5, 98.3, 35.76,67.5]])
np_2d

array([[1.73, 1.68, 1.71, 1.89, 1.79],
       [56.5, 76.5, 98.3, 35.76,67.5]])

np_2d.shape
(2, 5) #2 rows, 5 columns

np_2d[0][2] or np_2d[0,2]
means 1st row, 3rd element
=> 1.71




**PANDAS

In Pandas, rectangular data is represnted as data frame.
.head() returns first few rows of a data frame.
.info() returns names of columns and data types they contain.
.shape returns no.of rows followed by no. of columns.
.describe() contains numerical statistics like mean, median etc.
.values contain data values in a 2 dimensional numpy array.
.columns contain column names.
.index contains row no. or row names.

#Sorting
.sort_values(" ") : change the order of the rows by sorting them.
.sort_values([" ", " "]) : sort multiple varibales.
.sort_values([" ", " "], ascending=[True, False]) : sorting variables in ascending order.
["name"] : will just look at name column.
[[" ", " "]] : to select multiple columns.
dogs[" "] > 50 : subsetting rows.  (will get data type : bool)
dogs[dogs[" "] > 50] (will get list of all dogs greater than 50 cm)
dogs[dogs[" "] == " "] : subsetting rows on text data.
dogs[dogs[" "] > "2015-01-20"] : subsetting based on dates.
is_lab = dogs["breed"] == "Labrador"
is_brown = dogs["color"] == "Brown"
dogs[is_lab & is_brown] : subsetting based on multiple conditions.
is_black_or_brown = dogs["color"].isin(["Black","Brown")]
dogs[is_black_or_brown]

#Adding a new column
dogs["height_m"] = dogs["height_cm"] / 100
print(dogs)

bmi_lt_100 = dogs[dogs["bmi"] < 100]
bmi_lt_100_height = bmi_lt_100.sort_values("height_cm", ascending = False)
bmi_lt_100_height[["name", "height_cm", "bmi"]]






