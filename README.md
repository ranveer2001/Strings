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




#Summarizing Statistics
dogs["height_cm"].mean()    (.median(), .mode(), .min(), .max(), .var(), .std(), .sum(), .quantile())

The .agg() method  
def pct30(column):  (pct30 computes the 30th percentile of a data frame column)
    return column.quantile(0.3)
    
dogs["weight_kg"].agg(pct30) -> gives 30th percentile of the dogs weight
dogs[["weight_kg", "height_cm]].agg(pct30)

def pct40(column):  (pct40 computes the 40th percentile of a data frame column)
    return column.quantile(0.4)
    
dogs["weight_kg"].agg([pct30, pct40])

dogs["weight_kg"].cumsum() : gives cummulative sum also : (.cummax(), .cummin(), .cumprod())

#Counting

Dropping duplicate names : vet_visits.drop_duplicates(subset = "name")
Dropping duplicate pairs : unique_dogs = vet_visits.drop_duplicates(subset = ["name", "breed"])
                           print(unique_dogs)
                            
#Sorting while Counting
unique_dogs["breed"].value_counts()
unique_dogs["breed"].value_counts(sort = True)

#To turn counts into proportions
unique_dogs["breed"].value_counts(normalize = True)

#Summaries by group
dogs[dogs["color"] == "Black"]["weight_kg"].mean()
dogs[dogs["color"] == "Brown"]["weight_kg"].mean()

-> Grouped summaries :
dogs.groupby("color")["weight_kg].mean()

-> Multiple grouped summaries :
dogs.groupby("color")[weight_kg].agg([min, max, sum])

-> Grouping by multiple variables :
dogs.groupby(["color", "breed"])["weight_kg"].mean()

-> Many groups, many summaries :
dogs.groupby(["color", "breed"])[["weight_kg","height_cm" ].mean()

#Grouping by pivot table
dogs.pivot_table(values = "weight_kg", index = "color")

-> Multiple statistics :
dogs.pivot_table(values = "weight_kg", index = "color", aggfunc=[np.mean, np.median])

-> For two variables :
dogs.pivot_table(values= "weight_kg", index = "color", columns = "breed", fill_value = 0, margins = True) #fill_value = 0 puts 0 in place of missing data 
#Margins puts mean of all the values in the last row or column




**Setting a column as the index

dogs_ind = dogs.set_index("name")
print(dogs_ind)

#Removing an index
dogs_ind.reset_index()

#Dropping an index
dogs_ind.reset_index(drop = True)

#Indexes make subsetting easier 
Earlier : dogs[dogs["name"].isin(["Bella", "Stella"])]
Now : dogs_ind.loc[["Bella", "Stella"]]

#Index values don't need to be unique
dogs_ind2 = dogs.set_index("breed")
print(dogs_ind2)

#Subsetting on duplicated index values
dogs_ind2.loc["Labrador"]

#Multi-level indexes
dogs_ind3 = dogs.set_index(["breed", "color"])
print(dogs_ind3)

#Subset the outer level with a list
dogs_ind3.loc[["Labrador", "Chihuahua"]]

#Subset inner levels with a list of tupels
dogs_ind3.loc[[("Labrador", "Brown"), ("Chihuahua", "Tan")]]

#Sorting by index values
dogs_ind3.sort_index()

#Control sort_index
dogs_ind3.sort_index(level = ["color", "breed"], ascending= [True, False])

#Slicing the outer level index
dogs_srt.loc["Chow Chow" : "Poddle"] (final value poddle is included)

*Slicing doesn't work on inner level index

#Slicing the inner levels correctly
dogs_srt.loc[("Labrador", "Brown") : ("Schnauzer" , "Grey")]

#Slicing columns
dogs_srt.loc[;, "name" : "height_cm"]

#Slice twice
dogs_srt.loc[("Labrador", "Brown") : ("Schnauzer" , "Grey"), "name": "height_cm"]

#Slicing by dates
dogs.loc["2014-08-25" : "2016-09-16"]

"Slicing by partial dates"
dogs.loc["2014" : "2016"]



**HISTOGRAMS

import matplotlib as plt
dog_pack["height_cm"].hist()
plt.show()

#Adjust bins
dog_pack["height_cm"].hist(bins = 20)
plt.show

#Bar plots
avg_weight_by_breed = dog_pack.groupby("breed")["weight_kg"].mean()

avg_weight_by_breed.plt(kind = "bar")
plt.show()

avg_weight_by_breed.plt(kind = "bar", title = "Mean weight by dog breed")
plt.show()

#Line plots
sully.head()
sully.plot(x = "date", y = "weight_kg", kind = "line")
plt.show()

#Rotating axis labels
sully.plot(x = "date", y = "weight_kg", kind = "line", rot = 45)
plt.show()

#Scatter Plots
dog_pack.plot(x = "height_cm", y = "weight_kg", kind = "scatter")
plt.show()

#Layering Plots
dog_pack[dog_pack["sex"]=="F"]["height_cm"].hist()
dog_pack[dog_pack["sex"]=="M"]["height_cm"].hist()
plt.show()

#Add a legend
dog_pack[dog_pack["sex"]=="F"]["height_cm"].hist()
dog_pack[dog_pack["sex"]=="M"]["height_cm"].hist()
plt.legend(["F", "M"])
plt.show()

#Transparency
dog_pack[dog_pack["sex"]=="F"]["height_cm"].hist(alpha = 0.7)
dog_pack[dog_pack["sex"]=="M"]["height_cm"].hist(alpha = 0.7)
plt.legend(["F", "M"])
plt.show()

#Detecting missing values
dogs.isna()

#Detecting any missing values in any columns
dogs.isna().any()

#Counting missing values
dogs.isna().sum()

#Plotting missing values
import matplotlib as plt
dogs.isna().sum().plot(kind = "bar")
plt.show()

#Removing missing values
dogs.dropna()

#Replacing missing values
dogs.fillna(0)

#Creating data frames from list of dictionaries by row
new_dogs = pd.DataFrame(list_of_dicts)
print(new_dogs)

#Creating data frames from dict of list by columns
new_dogs = pd.DataFrame(dict_of_list)
print(new_dogs)

*CSV = comma-separated values

#Data Frame manipulation
new_dogs["bmi"] = new_dogs["weight_kg"] / (new_dogs["height_cm"]/100) ** 2
print(new_dogs)

#Data Frame to CSV
new_dogs.to_csv("new_dogs_with_bmi.csv")




**MERGING TABLES

#Inner Join
wards_census = wards.census(census, on = 'ward')
print(wards_census.head(4))

#Controlling suffixes
wards_census = wards.census(census, on = 'ward', suffixes = ('_ward', '_cen')) #Data on left column will be given suffixes _ward and on the right column _cen.
print(ward_census.head())
print(ward_census.shape)

One-to-One : Every row in the left table is realted to only one row in the right table.
One-to-many : Every row in the left table is related to one or many rows in the right table.

Single merge : grants.merge(licenses, on =['address', 'zip'])
Merging Multiple tables : grants.merge(licenses, on =['address', 'zip'])\.merge(wards, on='ward', suffixes=('_bus', '_ward'))
Three tables : df1.merge(df2, on='col') \.merge(df3, on='col')

#Merge with left join
movies_taglines = movies.merge(taglines, on='id', how = 'left')
print(movies_taglines.head())

#Merge with right join
tv_movies = movies.merge(tv_merge, how = 'right', left_on='id', right_on='movie_id')
print(tv_movies.head())

#Merge with outer join
family_comedy = family.merge(comedy, on='movie_id', how='outer', suffixes = ('_fam', '_com')
print(family_comedy)

#Merging a table with itself
original_sequels = sequels.merge(sequels, left_on='sequel', right_on='id', suffixes=('_org', '_seq))
print(original_sequels.head())

#Continue format results
print(original_sequels[['title_org','title_seq']].head()

#Merging itself with left join
original_sequels = sequels.merge(sequels, left_on='sequel', right_on='id', how='left', suffixes=('_org', '_seq))
print(original_sequels.head())

#Setting an index
movies = pd.read_csv('tmdb_movies.csv', index_col=['id'])
print(movies.head())

#Merging on index
movies_taglines = movies.merge(taglines, on='id', how='left')
print(movies_taglines.head())

#Multi-index merge
samuel_casts = samuel.merge(casts, on=['movie_id', 'cast_id']

#Index merge with left_on and right_on
movies_genres = movies.merge(movies_to_genres, left_on='id', left_index=True, right_on='movie_id', right_index=True)




**INTRODUCTION TO DATA VISUALIZATION USING MATLPOTLIB

import matlplotlib.pyplot as plt
fig, ax = plt.subplots()
plt.show()

#Adding data to axes
seattle_weather["MONTH"]
seattle_weather["MTLY-NORMAL"]

ax.plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL"])
plt.show()

#Adding markers
ax.plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL"], marker="o") (markers are rounded)
plt.show()

ax.plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL"], marker="v") (markers shaped like triangles)
plt.show()

#Setting the linestyle
ax.plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL"], marker="v", linestyle="--") (change appearance of line to dashed line)
plt.show()

ax.plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL"], marker="v", linestyle="None") (eliminating lines completely)
plt.show()

#Choosing color of data
ax.plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL"], marker="v", linestyle="--", color="r")
plt.show

#Customizing the axes labels
ax.set_xlabel("Time(months)")
plt.show()

#Setting the y label
ax.set_xlabel("Time(months)")
ax.set_ylabel("Average Temperature(Celcius degrees)")
plt.show()

#Adding a title
ax.set_title("Weather in Seattle")
plt.show

#Adding perecntile
ax.plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL-25PCTL"], marker="v", linestyle="--") 
plt.show()

#Small multiples with plt.subplots
fig, ax = subplots()
fig, ax = subplots(3,2) (3 rows and 2 columns)
plt.show()

ax[0].plot(seattle_weather["MONTH"], seattle_weather["MTLY-NORMAL-25PCTL"], marker="v", linestyle="--") )

#Sharing the y-axis range
fig, ax = plt.subplots(2,1, sharey=True) (Means both plos will have same rang of y values)

#Plotting Time-Series data
import matplotlib.pyplot as plt
fig,ax = subplots()
ax.plot(climate_change.index, climate_change['co2']

ax.set_ylabel('CO2(ppm)')
plt.show()

#Zooming in on a decade
sixties = climate_change["1960-01-01:"1969-12-31"]
ax.plot(sixties.index, sixties['co2']
ax.set_xlabel('Time')
ax.set_ylabel('CO2(ppm)')
plt.show()

#Plotting two time-series together
import matplotlib.pyplot as plt
fig,ax = subplots()
ax.plot(climate_change.index, climate_change['co2']
ax.plot(climate_change.index, climate_change['relative_temp']
ax.set_xlabel('Time')
ax.set_ylabel('CO2(ppm)/ Relative temperature')

#Using twin axes
fig,ax = subplots()
ax.plot(climate_change.index, climate_change["co2"])
ax.set_xlabel('Time')
ax.set_ylabel('CO2(ppm)')
ax2 = ax.twinx() (both have same x axis, but different y axis)
ax.plot(climate_change.index, climate_change['relative_temp'])
ax.set_ylabel('CO2(ppm)/ Relative temperature(Celsius)')

#Separating variables by color
fig,ax = subplots()
ax.plot(climate_change.index, climate_change["co2"], color="blue")
ax.set_xlabel('Time')
ax.set_ylabel('CO2(ppm)', color="blue")
ax2 = ax.twinx() (both have same x axis, but different y axis)
ax.plot(climate_change.index, climate_change['relative_temp'], color="red")
ax.set_ylabel('CO2(ppm)/ Relative temperature(Celsius)', color="red")

#Coloring the ticks
ax.tick_params('y', colors="blue")

#A function that plots time-series
def plot_timeseries(axes, x, y, color, xlabel, ylabel)
axes.plot(x, y, color=color)
axes.set_xlabel(xlabel)
axes.set_ylabel(ylabel, color=color)
axes.tick_params('y', colors=colors)

#Annotation
ax2.annotate(">1 degree", xy=[pd.TimeStamp("2015-10-06"),1])

#Positioning the annotated text
ax2.annotate(">1 degree", xy=(pd.TimeStamp("2015-10-06"),1), xytext=(pd.Timestamp('2008-10-06'),-0.2), arrowprops={})

#Customize arrow properties
ax2.annotate(">1 degree", xy=(pd.TimeStamp("2015-10-06"),1), xytext=(pd.Timestamp('2008-10-06'),-0.2), arrowprops={"arrowstyle":"->", "color":"gray"})


#BAR CHARTS
medals = pd.read_csv('medals_by_country_2016.csv', index_col=0)
fig,ax = subplots()
ax.bar(medals.index, medals["Gold"])
plt.show()

#Rotate the tick labels
fig, ax = plt.subplots()
ax.bar(medals.index, medals["Gold"])
ax.set_xticklabels(medals.index, rotation=90)
ax.set_ylabel("Number of medals")
plt.show()

#Stacking data on top of the other
fig, ax = plt.subplots()
ax.bar(medals.index, medals["Gold"])
ax.bar(medals.index, medals["Silver"], bottom = medals["Gold"])
ax.set_xticklabels(medals.index, rotation=90)
ax.set_ylabel("Number of medals")
plt.show()

#For three medals
fig, ax = plt.subplots()
ax.bar(medals.index, medals["Gold"])
ax.bar(medals.index, medals["Silver"], bottom = medals["Gold"])
ax.bar(medals.index, medals["Bronze"], medals["Gold"] + medals["Silver"])
ax.set_xticklabels(medals.index, rotation=90)
ax.set_ylabel("Number of medals")
plt.show()

#Adding a legend
fig, ax = plt.subplots()
ax.bar(medals.index, medals["Gold"], label = "Gold")
ax.bar(medals.index, medals["Silver"], bottom = medals["Gold"], label = "Silver")
ax.bar(medals.index, medals["Bronze"], medals["Gold"] + medals["Silver"], label = "Bronze")
ax.set_xticklabels(medals.index, rotation=90)
ax.set_ylabel("Number of medals")
ax.legend
plt.show()


#HISTOGRAMS
fig, ax = plt.subplots()
ax.hist(mens_rowing["Height"])
ax.hist(mens_gymnastic["Height"])
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations)
plt.show()

#Adding labels and bins
fig, ax = plt.subplots()
ax.hist(mens_rowing["Height"], label = "Rowing", bins = 5)
ax.hist(mens_gymnastic["Height"], label = "Gymnastics", bins = 5)
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations)
plt.show()

#Setting bin boundaries
fig, ax = plt.subplots()
ax.hist(mens_rowing["Height"], label = "Rowing", bins = [150, 160, 170, 180, 190, 200, 210])
ax.hist(mens_gymnastic["Height"], label = "Gymnastics", bins = [150, 160, 170, 180, 190, 200, 210])
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations)
plt.show()

#Change solid bars of histogram to thin lines(transparency)
fig, ax = plt.subplots()
ax.hist(mens_rowing["Height"], label = "Rowing", bins = [150, 160, 170, 180, 190, 200, 210], histtype = "step")
ax.hist(mens_gymnastic["Height"], label = "Gymnastics", bins = [150, 160, 170, 180, 190, 200, 210], histtyoe = "step")
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations)
plt.show()

#Statistical plotting
fig, ax = plt.subplots()
ax.hist("Rowing", mens_rowing["Height"].mean(), yerr= mens_rowing["Height"].std())
ax.hist("Gymnastics", mens_rowing["Height"].mean(), yerr= mens_rowing["Height"].std())
ax.set_ylabel("Height(cm)")
plt.show()

#Adding boxplots
fig, ax = plt.subplots()
ax.boxplot([mens_rowing["Height"], mens_gymnastics["Height"])
ax.set_xticklabels(["Rowing", "Gymnastics"])
ax.set_ylabel("Height(cm)")
plt.show()


#SCATTER PLOTS
fig, ax = subplots()
ax.scatter(climate_change["co2"], climate_change["relative_temp"])
ax.set_xlabel("CO2(ppm)")
ax.set_ylabel("Relative temp.(celsius)")
plt.show()

#Changing style of a plot
plt.style.use("ggplot")

#Back to the default
plt.style.use("default")

#The bmh style
plt.style.use("bmh")

#Seaborn styles
plt.style.use("seaborn-colorblind")

#Saving the figure to file
fig.savefig("gold_medals.png")

#Resolution
fig.savefig("gold_medals.png", dpi = 300)

#Size
fig.set_size_inches([5,3])

