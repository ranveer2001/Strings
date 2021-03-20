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
plt.show()

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




**INTRODUCTION TO SEABORN

Seaborn : Python data visualization library; easily creates most common types of plots.
          Works well with pandas data structures.
          Built on top of Matplotlib.
          
import seaborn as sns (sns = Samuel Norman Seaborn)
import matplotlib.pyplot as plt
height = [77, 78, 89, 90, 91, 99]
weight = [120, 130, 135, 168, 189, 190]
sns.scatterplot(x=height, y=weight) (scatterplot)
plt.show()

#Create a count plot
sns.countplot(x = gender)
plt.show()

#Using pandas with Seaborn
import pandas as pd
df = pd.read_csv("masculinity.csv")
df.head()

#Using data frames with countplot()
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv("masculinity.csv")
sns.countplot(x="how_masculine", data=df)
plt.show()

#A scatter plot with hue
import matplotlib.pyplot as plt
import seaborn as sns
sns.scatterplot(x="total_bill", y="tip", data=tips, hue="smoker")
plt.show()

#Setting hue order
import matplotlib.pyplot as plt
import seaborn as sns
sns.scatterplot(x="total_bill", y="tip", data=tips, hue="smoker", hue_order =["Yes", "No"])
plt.show()

#Specifying hue colors
import matplotlib.pyplot as plt
import seaborn as sns
hue_colors = {"Yes":"black", "No":"red"}
sns.scatterplot(x="total_bill", y="tip", data=tips, hue="smoker", palette=hue_colors)

#Using hue with countplots
import matplotlib.pyplot as plt
import seaborn as sns
sns.countplot(x="smoker", data=tips, hue="sex")
plt.show()

#Relplot()
Why use relplot() instead of scatterplot() ?
relplot() lets you create subplots in a single figure

import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", col="smoker") (subplots in columns, that's why col="smoker", for rows, row="smoker")
plt.show()

col_wrap
col_order
row_order

#Customizing scatter plots

*Subgroups with point size
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", size="size")
plt.show()

*Point size and hue
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", size="size", hue="size")
plt.show()

*Subgroups with point style
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", size="size", hue="size", style="smoker")
plt.show()

*Changing point transparency
(Set alpha to be between 0 and 1)
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", alpha=0.4)
plt.show()

#LINE PLOTS
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="hour", y="NO_2_mean", data=air_df_mean, kind="line")
plt.show()

*Subgroups by location and adding markers
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="hour", y="NO_2_mean", data=air_df_mean, kind="line", style="location", hue="location", markers=True)
plt.show()

*Turning off line style
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="hour", y="NO_2_mean", data=air_df_mean, kind="line", style="location", hue="location", markers=True, dashes=False)
plt.show()

*Replacing confidence interval with standard deviation
import matplotlib.pyplot as plt
import seaborn as sns
sns.relplot(x="hour", y="NO_2", data=air_df_mean, kind="line", ci="sd")
plt.show()

#catplot()
-> catplot() is used to create categorical plots.
-> Same advantages of relplot()

import matplotlib.pyplot as plt
import seaborn as sns
sns.catplot(x="how_masculine", data=masculinity_data, kind="count")
plt.show()

*Changing the order
import matplotlib.pyplot as plt
import seaborn as sns
Category_order = ["No answer", "Not at all", "Some what"]
sns.catplot(x="how_masculine", data=masculinity_data, kind="count", order=category_order)
plt.show()

*Bar plots using catplots
import matplotlib.pyplot as plt
import seaborn as sns
sns.catplot(x="day", y="total_bill", data=tips, kind="bar")
plt.show()

*Turning off confidence intervals
import matplotlib.pyplot as plt
import seaborn as sns
sns.catplot(x="day", y="total_bill", data=tips, kind="bar", ci=None)
plt.show()

#BOX PLOTS
import matplotlib.pyplot as plt
import seaborn as sns
g = sns.catplot(x="time", y="total_bill", data=tips, kind="box")
plt.show()

*Changing the whiskers using whis
import matplotlib.pyplot as plt
import seaborn as sns
g = sns.catplot(x="time", y="total_bill", data=tips, kind="box", whis=[0, 100])
plt.show()

#POINT PLOTS
import matplotlib.pyplot as plt
import seaborn as sns
sns.catplot(x="age", y="masculinity_important", data=masculinity_data, hue="feel_masculine", kind="point")
plt.show()

*Disconnecting the points
import matplotlib.pyplot as plt
import seaborn as sns
sns.catplot(x="age", y="masculinity_important", data=masculinity_data, hue="feel_masculine", kind="point", join=False)
plt.show()

*Displaying median
import matplotlib.pyplot as plt
import seaborn as sns
from numpy import median
sns.catplot(x="smoker", y="total_bill", data=tips, kind="point", estimator=median)
plt.show()

*Customizing the confidence intervals
capsize=0.2 etc


#Changing Plot styles and color

*Figure style: "Whitegrid"
sns.set_style("whitegrid")
import matplotlib.pyplot as plt
import seaborn as sns
sns.catplot(x="age", y="masculinity_important", data=masculinity_data, hue="feel_masculine", kind="point")
plt.show()

*Other Styles
sns.set_style("ticks")
sns.set_style("dark")
sns.set_style("darkgrid")

*Figure "palette" changes the color of the main elements of the plot
sns.set_palette()

*Diverging palette
sns.set_palette("RdBu")

*Custom palettes
custom_palette = ["red", "green", "orange", "blue", "yellow", "purple"]
sns.set_palette(custom_palette)

*Enlarged context
sns.set_context("talk")



#DEFINING A FUNCTION

def square(value):
    new_value = value ** 2
    print(new_value)
    
square(4)
16

Also,
def raise_to_power(value1, value2)
new_value = value1 ** value2
return new_value

or,
def raise_both(value1, value2)

*Scope : part of the program where an object or name may be accesible
-> Global scope : defined in the main body of the script
-> Local scope : defined inside a function
-> Built-in scope : names in the pre-defined built-ins module


**INTRODUCTION TO SEABORN

import matplotlib.pyplot as plt
import pandas as pd
df = pd.read_csv("wines.csv")
fig, ax = plt.subplots()
ax.hist(df['alcohol'])

#Pandas

import pandas as pd
df = pd.read_csv("wines.csv")
df['alcohol'].plot.hist()

#Seaborn

-> The distplot is similar to the histogram shown in previous examples.
-> By default, it generates a Gaussian Kernel Density Estimate(KDE)

import seaborn as sns
sns.distplot(df['alcohol'])

*Creating a distplot histogram
sns.distplot(df['alcohol'], kde=False, bins=10)

OR

sns.distplot(df['alcohol'], hist=False, rug=True)

*Further Customizations
sns.distplot(df['alcohol'], hist=False, rug=True, kde_kws = {'shade':True})



**REGRESSION PLOTS IN SEABORN

The regplot function generates a scatter plot with a regression line.
sns.regplot(x="alcohol", y="pH", data=df)

*Lmplot() builds on top of the base regplot()
regplot() - low level
lmplot() - high level

sns.lmplot(x="alcohol", y="pH", data=df)

*lmplot faceting
Organize data by colors(hue)
Orgainize data by columns(col)


#Setting Seaborn  Style
-> Seaborn has default configurations that can be applied with sns.set().

sns.set()
df['Tuition'].plot.hist()

*Theme examples with sns.set_style()
for style in ['white','dark','whitegrid','darkgrid','ticks']:
sns.set_style(style)
sns.distplot(df['Tuition'])
plt.show()

*Remove axes with despine()
sns.set_style('white')
sns.distplot(df['Tuition'])
sns.despine(left=True)



**CATEGORICAL PLOT TYPES

sns.stripplot(data=df, y="DRG Definition", x="Average Covered Charges", jitter=True)
sns.swarmplot(data=df, y="DRG Definition", x="Average Covered Charges")
sns.boxplot(data=df, y="DRG Definition", x="Average Covered Charges") #Abstract Representation
sns.violinplot(data=df, y="DRG Definition", x="Average Covered Charges") #Combination of density and boxplot for alternative view
sns.lvplot(data=df, y="DRG Definition", x="Average Covered Charges") #letter value plot scales more effectively to large datasets
sns.barplot(data=df, y="DRG Definition", x="Average Covered Charges", hue="Region") #Statistical estimates
sns.pointplot(data=df, y="DRG Definition", x="Average Covered Charges", hue="Region") #Useful to check how values change across categorical data
sns.countplot(data=df, y="DRG Definition", hue="Region") #Gives number of instances of each variable


**REGRESSION PLOTS

*Plotting with regplot()
sns.regplot(data=df, x='temp', y='total_rentals', marker='+')

*residplot()
-> It is useful for evaluating the fit of a model.
sns.residplot(data=df, x='temp', y='total_rentals')

*Ploynomial regression
-> It is done using the order parameter.
sns.regplot(data=df, x='temp', y='total_rentals',order=2)

*residplot with polynomial regression
sns.residplot(data=df, x='temp', y='total_rentals',order=2)

*Categorical values
sns.regplot(data=df, x='temp', y='total_rentals', x_jitter=.1, order=2)

*x_estimator can be useful for highlighting trends
sns.regplot(data=df, x='temp', y='total_rentals', x_estimator=np.mean, order=2)

*x_bins can be used to divide the data into discrete bins
sns.regplot(data=df, x='temp', y='total_rentals', x_bins=4)



**MATRIX PLOTS

* Seaborn's heatmap() function requires data to be in a grid format.
* pandas crosstab() is frequently used to manipulate the data.

pd.crosstab(df["mnth"], df["weekday"], values = df["total_rentals"], aggfunc='mean').round(0)
sns.heatmap(pd.crosstab(df["mnth"], df["weekday"], values = df["total_rentals"], aggfunc='mean'))

*Customize a heatmap
sns.heatmap(df_crosstab, annot=True, fmt="d", cmap="YlGnBu", cbar= False, linewidths=.5)

*Plotting a correlation matrix
Pandas corr function calculates correlations between columns in a dataframe.
sns.heatmap(df.corr())

**PAIR GRIDS AND PLOTS

*Creating a pairgrid
g = sns.PairGrid(df, vars=["abc", "dfd"])
g = g.map(plt.scatter)

*Customizing PairGrid diagonals
g = g.map_diag(plt.hist)
g = g.map_offdiag(plt.scatter)

*Pairplot is a shortcut for PairGrid
sns.pairplot(df, vars=["abc", "dfd"], kind="reg", diag_kind="hist")




**IMPORTING DATA IN PYTHON

*Reading a file
filename = "abc"
file = open(filename, mode='r')
text = file.read()
file.close

*Writing to a file
filename = "abc"
file = open(filename, mode='w')
file.close

*Alternative way 
with open('abc', 'r') as file :
print(file.read())

#How do you import flat files?
1) Numpy
2) pandas

*Importing flat files using Numpy
->They are standard for storing numerical data
-> Essential for other packages like scikit-learn

import numpy as np
filename = 'MNST.txt'
data = np.loadtxt(filename, delimiter = ',')
data

*Customizing numpy import
import numpy as np
filename = 'MNST.txt'
data = np.loadtxt(filename, delimiter = ',', skiprows = 1)
print(data)

*For just 1st and 3rd columns use : usecols=[0, 2]
*Using different data types : dtype = str

*Importing flat files using pandas
import pandas as pd
filename = 'winequality-red.csv'
data = pd.read_csv(filename)
data.head()

*PICKLED FILES
import pickle
with open('pickled_fruit.pkl', 'rb') as file:   (rb means read only and binary file)
     data = pickled.load(file)
print(data)

*Importing Excel spreadsheets
import pandas as pd
file = 'urbanpop.xlsx'
data = pd.Excelfile(file)
print(data.sheet_names)

df1 = data.parse('1960-1966')  (sheet name as a string)
df2 = data.parse(0)  (sheet name as a float)

*SAS files
SAS : Statistical Analysis System

*Importing SAS files
import pandas as pd
from sas7bdat import SAS7BDAT
with SAS7BDAT ('urbanpop.sas7bdat') as file :
     df_sas = file.to_data_frame()
     
*Importing Stata file
import pandas as pd
data = pd.read_stata('urbanpop.dta')

*HDF5
Hierarchical Data Format Version 5

*Importing HDF5 files
importing h5py
filename = 'ayeueila.hdf5'
data = h5py.File(filename, 'r')
print(type(data))

*MATLAB
Matrix Laboratory

SciPy helps in reading matlab files
-> scipy.io.loadmat() - read .mat files
scipy.io.savemat() - write .mat files

*Importing a .mat file
import scipy.io
filename = 'workspace.mat'
mat = scipy.io.loadmat(filename)
print(type(mat))


**CREATING A DATABASE ENGINE

*SQLite database
-> Fast and simple

*SQLAlchemy
-> Works with many relational Database management systems

from sqlalchemy import create_engine
engine = create_engine('sqlite://Northwind.sqlite')
table_names = engine.table_names()
print(table_names)

*BASIC SQL query
SELECT * FROM Table_name
-> Returns all columns of all rows of the table

SELECT * FROM Orders

*First SQL query
from sqlalchemy import create_engine
import pandas as pd
engine = create_engine('sqlite://Northwind.sqlite')
con = engine.connect()
rs = con.execute("SELECT * FROM Orders")
df = pd.DataFrame(rs.fetchall())
con.close()

*Set the dataframe column names
df.columns = rs.keys()

*Pandas way to query the code as above
df = pd.read_sql_query("SELECT * FROM Orders", engine)

*Advanced queries-(Inner join in Python(Pandas))
from sqlalchemy import create_engine
import pandas as pd
engine = create_engine('sqlite://Northwind.sqlite')
df = pd.read_sql_query("SELECT OrderID, Company Name FROM Orders INNER JOIN customers on Orders.CustomerID = Customer.CustomerID", engine)
print(df.head()




**IMPORTING FLAT FILES FROM THE WEB

-> urlopen() : accepts URLs instead of file names

*Automate file download in Python
from urllib.request import urlretrieve
url = 'ahashshhsdhdjd/winequality-white.csv'
urlretrieve(url, 'winequality-white.csv')

*Ingredients of URL :
-> Protocol identifier : http:
-> Resource name : datacamp.com

*HTTP requests to import files from the web
-> HTTP : HyperText Transfer Protocol

*GET requests using urllib
from urllib.request import urlopen, Request
url = "https://www.wikipedia.com/"
request = Request(url)
response = urlopen(request)
html = response.read()
response.close()

*GET requests using requests
import requests
url = "https://www.wikipedia.com"
r = requests.get(url)
text = r.text

*Scraping the web in python
-> HTML : HyperText Markup language
-> Mix of structured and unstructured data

*Beautiful soup
-> Parse and extract structured data from HTML

from bs4 import BeautifulSoup
import requests
url = 'jsjsjd'
r = requests.get(url)
html_doc = r.text
soup = BeautifulSoup(html_doc)

*Exploring BeautifulSoup
print(soup.title)
print(soup.get_text())

for link in soup.find_all('a'):
    print(link.get('href'))
    
*Introduction to API And JSONs

API : Application Programming interface

JSONs : Javascript Object Notation

*Loading JSONs in Python
import json
with open('snakes.json', 'r') as json_file:
     json_data  = json.load(json_file)



**DATA TYPE CONSTRAINTS

*String to integers
sales['Revenue'] = sales['Revenue'].astype('int')

*Numeric to Categorical
df['marriage_status'] = df['marriage_status'].astype('category')

*Uniqueness constraints
How to find duplicate values?
duplicates = height_weight.duplicated()
print(duplicates)

*Column names to look for duplicates
column_names = ['first_name', 'last_name', 'address']
duplicates = height_weight.duplicated(subset = column_names, keep = False)

*Drop duplicates
height_weight.drop_duplicates(inplace = True)

*Output duplicate values
column_names = ['first_name', 'last_name', 'address']
duplicates = height_weight.duplicated(subset = column_names, keep = False)
height_weight[duplicates].sort_values(by = 'first_name')

*Group by column names and produce statistical summaries
column_names = ['first_name', 'last_name', 'address']
summaries = {'height':'max', 'weight':'mean'}
height_weight = height_weight.groupby(by = column_names).agg(summaries).reset_index()


*Finding inconsistent categories
inconsistent_categories = set(study_data['blood_type']).difference(categories['blood_type'])
print(inconsistent_categories )

inconsistent_categories = study_data['blood_type'].isin(inconsistent_categories)

*Dropping inconsistent categories
inconsistent_categories = set(study_data['blood_type']).difference(categories['blood_type'])
inconsistent_categories = study_data['blood_type'].isin(inconsistent_categories)
consistent_data = study_data[~ inconsitent_categories]


*Cleaning text data
*Fixing the phone number column
phones["Phone number"] = phones["Phone number"].str.replace("+", "00")
phones

*Replace phone numbers with lower than 10 digits to NaN
digits = phones['Phone number'].str.len()
phones.loc[digits < 10, "phone number"] = np.nan
phones

*Fixing the phone number column
sanity_check = phone['Phone number'].str.len()
assert sanity_check.min() >= 10
assert phone['Phone number'].str.contains("+|-").any() == False  (assert returns nothing if the condition passes)



**UNIFORMITY

*Treating Temperature data
temp_fah = temperatures.loc[temperatures['Temperature'] > 40, 'Temperature']
temp_cels = (temp_fah - 32) * (5/9)
temperatures.loc[temperatures['Temperature'] > 40, 'Temperature'] = temp_cels
assert temperatures['Temperature'].max() < 40

*Treating date data
birthdays['Birthday'] = pd.to_datetime(birthday['Birthday'], infer_datetime_format = True, errors = 'coerce')


**COMPARING STRINGS

*Simple string comparison
from fuzzywuzzy import fuzz
fuzz.WRatio('Reeding','Reading') #Comparing reeding vs reading

*Partial string comparison
fuzz.WRatio('Houston Rockets', 'Rockets')

*Partial string comparison with different order
fuzz.WRatio('Houston Rockets vs Los Angeles Lakers', 'Lakers vs Rockets')

*Comparison with arrays
from fuzzywuzzy import fuzz
string = "Houston Rockets vs Los Angeles Lakers"
choices = pd.Series(['Rockets vs Lakers', 'Lakers vs Rockets', 'Heat vs Bulls')]
process.extract(string, choices, limit = 2)

*GENERATING PAIRS
import Recordlinkage
indexer = recordlinkage.Index()
indexer.block('state')
pairs = indexer.index(census_A, census_B)

*Finding the only pairs we want
potential_matches[potential_matches.sum(axis = 1) => 2]




**DATES IN PYTHON

from datetime import date
two_hurricanes_date = [date(2016,10,7), date(2017,6,21)]

*Attributes of a date
from datetime import date
two_hurricanes_date = [date(2016,10,7), date(2017,6,21)]
print(two_hurricanes_date[0].year). #2016
print(two_hurricanes_date[0].month). #10
print(two_hurricanes_date[0].day).  #7

*Finding the weekday of a date
print(two_hurricanes_date[0].weekday())

*Math with dates
from datetime import date
d1 = date(2017,11,5)
d2 = date(2017,12,4)
l = [d1, d2]
print(min(l))

#Subtract two dates
delta = d2 - d1
print(delta.days)
=29

*Turning date into strings

#ISO 8601 FORMAT
from datetime import date
d = date(2017,11,5)
print(d)

*Putting ISO format in a list
print([d.isoformat()])

*strftime*
d = date(2017,1,5)
print(d.strftime("%Y"))
2017
print(d.strftime("Year is %Y") (Also, %Y/%m/%d)
Year is 2017

*Dates and Time
from datetime import datetime
dt = datetime(year=2017, month=10, day=1, hour=15, minute=23, second=25, microsecond=500000)
print(dt)
2017-10-01 15:23:25.500000

dt_hr = dt.replace(minute=0, second=0, microsecond=0)
print(dt_hr)
2017-10-01 15:00:00

*Printing datetimes
print(dt.strftime("%Y-%m-%d %H:%M:%S))

*Working with durations
start = datetime(2017,10,8,23,46,47)
end = datetime(2017,10,9,0,10,57)
duration = end - start
print(duration.total_seconds())

*Creating timedeltas
from datetime import timedelta
delta1 = timedelta(seconds=1)
print(start)
print(start + delta1)

*UTC Offsets
from datetime import datetime, timedelta, timezone
ET = timezone(timedelta(hours=-5))
dt = datetime(2017,12,30,15,9,3,tzinfo = ET)

IST = timezone(timedelta(hours=5, minutes=30))
print(dt.astimezone(IST))

*Time zone database
from datetime import datetime
from dateutil import tz
et = tz.gettz('America/New_York) #Format : 'Continent/City

*Start of daylight savings time
spring_ahead_159am = datetime(2017,3,12,1,59,59)
spring_ahead_159am.isoformat()

spring_ahead_3am = datetime(2017,3,12,3,0,0)
spring_ahead_3am.isoformat()

(spring_ahead_3am - spring_ahead_159am).total_seconds()

*Dateutil
from dateutil import tz
eastern = tz.gettz('America/New York')
spring_ahead_159am = datetime(2017,3,12,1,59,59,tzinfo=eastern)
spring_ahead_3am = datetime(2017,3,12,3,0,0,tzinfo=eastern)

*Ending Daylight Savings Time
eastern = tz.gettz('US/Eastern')
first_1am = datetime(2017,11,5,1,0,0,tzinfo = eastern)
tz.datetime_ambigous(first_1am)

second_1am = datetime(2017,11,5,1,0,0,tzinfo=eastern)
second_1am = tz.enfold(second_1am)

*Summarizing data in pandas
rides['Duration'].mean()
rides['Duration'].sum()
rides['Duration'].sum()/ timedelta(days=91)
rides['Member type'].value_counts()
rides.groupby('Member type').size() #size per group
rides.groupby('Member type').first() #First ride per group

*Summarizing datetime in Pandas
rides\.resample('D', on='Start date')\['Duration Seconds']\.mean()\.plot()



**DOCSTRINGS

*Anatomy of a docstring
def function_name(arguements) :
"""
Description of what the function does.
Description of the arguements, if any.
Description of the return value(s), if any.
Description of errors raised, if any.
Optional extra notes.
"""

*Google style-arguements
def function(arg_1, arg_2=42):
"""Description of what the function does

Args :
arg_1(str): Description of arg_1 that can break onto the next line if needed.
arg_2(int, optional): Write optional when an arguement has a default value.

*Google style - return values
def function(arg_1, arg_2=42):
"""Description of what the function does

Args :
arg_1(str): Description of arg_1 that can break onto the next line if needed.
arg_2(int, optional): Write optional when an arguement has a default value.

Returns:
bool: Optional description of the return value
Extra lines are not idented
"""

*Numpydoc
def function(arg_1, arg_2=42):
"""
Description of what the function does

Parameters
--------

arg_1 : expected type of arg_1
        Description of arg_1
arg_2 : int, optional
        Write optional when an arguement has default value
        Default = 42

Returns
-------
The type of the return value
        Can include a description of the return value.
        Replace "Returns" with "Yields" if this function is a generator.
"""

*Retrieving docstrings
def the_answer():
"""Return the answer to life, the universe , and everything.

Returns:
   int
"""
return 42
print(the_answer.__doc__)

import inspect
print(inspect.getdoc(the_answer))

*Surprising Examples of functions
def foo(x):
    x[0] = 99
my_list = [1, 2, 3]
foo(my_list)
print(my_list)
[99,2,3]

def bar(x):
    x = x + 90
my_var = 3
bar(my_var)
print(my_var)
3

*CONTEXT MANAGER
It sets up a context, runs your code and then removes the context.

*Using a context manager
with <context-manager> (<args>) as <variable-name> :
      #Run your code here
      #This code is running inside the context
      #This code runs after the context is removed
      
with open('my_file.txt') as my_file:
     text = my_file.read()
     length = len(text)
     
print('The file is {} charcters long'.format(length))

*How to create a context manager
@contextlib.contextmanager
def my_context :
    # Add any set up code you need
    yield
    # Add any teardown code you need
    
*The 'yield' keyword
@contextlib.contextmanager
def my_context :
    print('hello')
    yield
    print('goodbye')
    
with my_context() as foo:
     print('foo is {}'.format(foo))
     
hello
foo is 42
goodbye



**EXPLORATORY DATA ANALYSIS IN PYTHON

*DATAFRAMES AND SERIES
*Reading data

import pandas as pd
nsfg = pd.read_hdf('nsfg.hdf5', 'nsfg')
type(nsfg)

nsfg.head()

#Each column is a series
pounds = nsfg['birthwgt_lb1']
type(pounds)

*Arithmetic with Series
birth_weight = pounds + ounces/16.0
birth_weight.describe()

*Probability Mass functions
pmf_educ = Pmf(educ, normalize=False)
pmf_educ.head()
pmf_educ[12] shows the total no. of respondants at 12 years of education

pmf_educ = Pmf(educ, normalize=True)
pmf_educ.head()
#This is a normalized pmf and the frequencies add up to 1
pmf_educ[12] in this result is a fraction

*Plotting pmf as bar chart
pmf_educ.bar(label='educ')
plt.xlabel('Years of education')
plt.ylabel('PMF')
plt.show()

PMF(Probability Mass Function) is the probability that you get exactly x.
CDF(Cumulative Distribution Function) is the probability that you get a value <= x.

*Evaluating the CDF
q = 51
p = cdf(q)
print(p)

*Evaluating the inverse CDF
p = 0.25
q = cdf.inverse(p)
print(q)

*Normal distribution
sample = np.random.normal(size=1000)
Cdf(sample).plot()

*Normal CDF
from sciy.stats import norm
xs = np.linspace(-3,3)
ys = norm(0,1).cdf(xs)
plt.plot(xs,ys,color='gray')
Cdf(sample).plot()

*The bell curve
xs = np.linspace(-3,3)
ys = norm(0,1).pdf(xs)
plt.plot(xs,ys,color='gray')

*KDE plot
import seaborn as sns
sns.kdeplot(sample)

*PMF,CDF,KDE
-> Use CDFs for exploration.
-> Use PMFs if there are a small number of unique values.
-> Use KDE if there are a lot of values.


*Box plot
sns.boxplot(x='Age', y='gshsh', data=data, whis=10)
plt.show()

*Log scale
sns.boxplot(x='Age', y='gshsh', data=data, whis=10)
plt.yscale('log')
plt.show()

*Correlation coefficient
columns = ['HTM4', 'WTKG3', 'AGE']
subset = brfss[columns]
subset.corr()

*Linear regression
from scipy.stats import linregress
res = linregress(xs,ys)

*Regression lines to get line of best fit
fx = np.array([xs.min(), xs.max()])
fy = res.intercept + res.slope * fx
plt.plot(fx, fy, '-')

#dropna is used to remove the rows that are missing the data we need.

subset = brfss.dropna(subset=['WTKG3', 'HTM4'])
xs = subset['HTM4']
ys = subset['WTKG3']
res = linregress(xs, ys)
fx = np.array([xs.min(), xs.max()])
fy = res.intercept + res.slope * fx
plt.plot(fx, fy, '-')

*Multiple regression
import statsmodels.formula.api as smf
results = smf.ols('INCOME2 ~ _VEGESU1', data=brfss).fit() (ols = ordinary least squares)
results.params (It contains estimated slope and intercept)

*Adding age
results = smf.ols('realinc ~ educ + age', data=gss).fit()
results.params

*Adding a quadratic term
gss['age2'] = gss['age'] ** 2
model = smf.ols('realinc ~ educ + age + age2', data=gss)
results=model.fit()
results.params

*Generating predictions
df = pd.DataFrame()
df['age'] = np.linspace(18,85)
df['age2'] = df['age'] ** 2
df['educ'] = 12
df['educ2'] = df['educ'] ** 2
pred12 = results.predict(df)

*Plotting predictions
plt.plot(df['age'], pred12, abel='High School')
plt.plot(mean_income_by_age, 'o', alpha=0.5)

*Logistic regression
formula = 'realinc ~ educ + educ2 + age + age2 + C(sex)' #C indicates sex is a categorical variable
results = smf.ols(formula, data=gss).fit()
results.params

*Boolean variable
gss['gunlaw'].value_counts()
gss['gunlaw'].replace([2],[0],inplace=True)
gss['gunlaw'].value_counts()

*logistic regression
formula = 'realinc ~ educ + educ2 + age + age2 + C(sex)' #C indicates sex is a categorical variable
results = smf.logit(formula, data=gss).fit()
results.params

*Visualizing results
grouped = gss.groupby()
favor_by_age = grouped['gunlaw'].mean()
plt.plot(favor_by_age,'o',alpha=0.5)

plt.plot(df['age'],pred1,label='Male')
plt.plot(df['age'],pred2,label='Female')

plt.xlabel(Age')
plt.ylabel('ajsj')
plt.legend()


*Binomial distribution

n_deafults = np.random.binomial(n=100, p=0.05, size=1000)



**OPTIMAL PARAMETERS

*Checking Normality of Michelson Data
import numpy as np
import matplotlib.pyplot as plt
mean = np.mean(michelson_speed_of_light)
std = np.std(michelson_speed_of_light)
samples = np.random.normal(mean, std, size=100000)

*Linear regression by least squares with np.polyfit()
slope, intercept = np.polyfit(total_votes, dem_share, 1) (1 is the degree of polynomial you wish to fit)
slope
intercept

*Resampling engine
import numpy as np
np.random.choice([1,2,3,4,5], size=5)

*Computing a bootstrap replicate
bs_sample = np.random.choice(michelson_speed_of_light, size=100)
np.mean(bs_sample)

*Generating a pairs bootstrap sample
np.arrange(7)
inds = np.arrange(len(total_votes))
bs_inds = np.random.choice(inds,len(inds))
bs_total_votes = total_votes[bs_inds]
bs_dem_share = dem_share[bs_inds]




**SUPERVISED LEARNING WITH SCIKIT LEARN

What is Machine Learning?
-> It is the art and science of giving computers the ability to learn to make decisions from data without being explicitly programmed.
Examples : Learning to predict whether an email is spam or not; Clustering wikipedia entries into different categories.
-> Supervised learning : Uses labeled data
-> Unsupervised learning : Uses unlabeled data

*Unsupervised learning
-> Uncovering hidden pattern from unlabeled data
Example : Grouping customers into distinct categories (Clustering)

*Reinforcement learning
-> Software agents interact with an environment; learn how to optimize their behaviour given a system of rewards and punishments.
Applications : Economics, game playing, genetics

*Supervised learning
-> There is predictor variables and a target variable.
Aim : predict the target variable, given the  predictor variables.
Features = predictor variables = independent variables
Target variable = dependent variable = response variable

*The IRIS dataset in scikit-learn
from sklearn import datasets
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
plt.style.se('ggplot')
iris = datasets.load_iris()
type(iris)
print(iris_keys())
iris.data.shape
(150,4)
iris.target_names

*Exploratory data analysis(EDA)
X = iris.data
Y = iris.arget
df = pd.DataFrame(X, columns=iris.feature_names)
print(df.head())

*Visual EDA
_ = pd.plotting.scatter_matrix(df, c = y, figsize = [8,8], s = 50, marker = 'D') (c is color and s is shape)

*K-Nearest Neighbors(KNN)
-> It predicts the label of a data point by looking at the 'k' closest labeled data points , taking majority vote.

*Training a model on the data = 'fitting' a model to the data
.fit() method is used
.predict() method to predict the labels of new data

*Using scikit learn to fit a classifier
from sklearn.neighbors import KNeighborsClassifier
knn = KNeighborsClassifier(n_neighbour = 6)
knn.fit(iris['data'], iris['target'])
iris['data'].shape
(150,4)
iris['target'].shape
(150,)

*Predicting on unlabeled data
X_new = np.array([[5.6, 2.8, 3.9, 1.1], 
        [5.7, 2.6, 3.8, 1.3],
        [4.7, 3.2, 1.3, 0.2]])
   
prediction = knn.predict(X_new)
X_new.shape
(3,4)
print('Prediction :{}'.format(prediction))
Prediction : [1 1 0]

*Measuring Model performance

*Train/Test split
from sklearn.model_selection import train_test_split
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 21, stratify = Y)
knn = KNeighborsClassifier(n_neighbors = 8)
knn.fit(X_train, Y_train)
Y_pred = knn.predict(X_test)
print(\"Test et predictions :\\n {}\"format(Y_pred)
knn.score(X_test, Y_test) (It predicts the accuracy of the model)

*Model complexity
-> Larger k : smoother decision boundary = less complex model
-> Smaller k : more complex model = can lead to overfitting

*Introduction to egression

*Creating feature and target arrays
X = boston.drop('MEDV', axis=1).values
y = boston['MEDV'].values

*Predicting house value from a single feature
X_rooms = X[:,5]
type(X_rooms) type(y)
y = y.reshape(-1,1)
X_rooms = X_rooms.reshape(-1,1)

*Plotting house value vs no. of rooms
plt.scatter(X_rooms, y)
plt.ylabel('Value of house/100($)')
plt.xlabel'Number of rooms')
plt.show();

*Fitting a regression model
import numpy as np
from sklearn.linear_model import LinearRegression

reg = LinearRegression()
reg.fit(X_rooms,y)
prediction_space = np.linspace(min(X_rooms), max(X_rooms)).reshape(-1, 1)

plt.scatter(X_rooms, , color=blue')
plt.plot(prediction_space, reg_predict(prediction_space), color = 'black', linewidth = 3)
plt.show()

*Linear regression on all features
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
reg_all = LinearRegression()
reg_all.fit(X_train, Y_train)
Y_pred = reg_all.predict(X_test)
reg_all.score(X_test, Y_test)

*Cross validation in scikit-learn
from sklearn.model_selection import cross_val_score
from sklearn.linear_model import LinearRegression
reg = LinearRegression()
cv_results = cross_val_score(reg, X, Y, cv =5) (cv is no.of folds required)
print(cv_results)

*Regularized Regression
-> Large coefficients can lead to overfitting; penalizing large coefficients is called regularization.

*Ridge Regression in scikit learn
-> Ridge Regression is a technique for analyzing multiple regression data that suffer from multicollinearity.

from sklearn.linear_model import Ridge
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
ridge = Ridge(alpha = 0.1, normalize = True) (normalize = True ensures that all variables are on the same scale)
ridge.fit(X_train, Y_train)
ridge_pred = ridge.predict(X_test)
ridge.score(X_test, Y_test)

*Lasso Regression in scikit-learn
-> In statistics and machine learning, lasso is a regression analysis method that performs both variable selection and regularization in order to enhance the prediction accuracy and interpretability of the resulting statistical model.

from sklearn.linear_model import Ridge
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
lasso = lasso(alpha = 0.1, normalize = True) (normalize = True ensures that all variables are on the same scale)
lasso.fit(X_train, Y_train)
lasso_pred = lasso.predict(X_test)
lasso.score(X_test, Y_test)

-> Lasso regression shrinks the coefficients of less important features to exactly 0.

*Lasso for feature selection in scikit-learn
from sklearn.linear_model import Lasso
names = boston.drop('MEDV', axis = 1).columns
lasso = lasso(alpha = 0.1)
lasso_coef = lasso.fit(x, y).coef_
_ = plt.plot(range(len(names)), lasso_coef)
_ = plt.xticksrange(len(names)), names, rotation=60)
_ = plt.ylabel('Coefficients')
plt.show()


*Confusion matrix in scikit-learn
from sklearn.metrics import classification_report
from sklearn.metrics import confusion_matrix
knn = KNeighborsClassifiers(n_neighbors = 8)
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.4, random_state = 42)
knn.fit(X_train, Y_train)
y_pred = knn.predict(X_test)

*Logistic Regression
It outputs probabilities.
If the probability 'p' is greater than 0.5 :
The data is labeled as '1'
If the probability 'p' is less than 0.5:
The data is labeled as '0'

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
logreg = LogisticRegression()
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
logreg.fit(X_train, Y_train)
Y_pred = logreg.predict(X_test)

-> By default, logistic regression threshold is 0.5

*Reciever Operating Characteristic curve (ROC curve)
*Plotting the ROC curve
from sklearn.metrics import roc_curve
y_pred_prob = logreg.predict_proba(X_test)[:,1]
fpr, tpr, threshold = roc_curve(y_test y_red_prob)
plt.plot([0,1], [0,1], 'k--')
plt.plot(fpr, tpr, label='Logistic Regression')
plt.xlabel('False Positive Rate')
plt.ylabel('True Positive Rate')
plt.title('Logistic Regression ROC curve')
plt.show();

*Precision = TP / (TP + FP)
*Recall = TP/ (TP + FN)

-> Larger area under ROC curve = better model

*Area under ROC curve(AUC)
from sklearn.metrics import roc_auc_score
logreg = LogisticRegression()
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
logreg.fit(X_train, Y_train)
y_pred_prob = logreg.predict_proba(X_test)[:,1]
roc_auc_score(y_test, y_pred_prob)

*AUC using cross-validation
from sklearn.model_selection import cross_val_score
cv_scores = cross_val_scores(logreg X, Y, cv = 5, scoring='roc_auc')
print(cv_scores)

*Hyperparameters tuning
-> Parameters like alpha and k: Hyperparameters
-> Hyperparameters cannot be learned by fitting the model

*GridSearch CV in scikit-learn
from skearn.model_selection import GridSearchCV
param_grid = {'n_neighbors':np.arrange(1, 50)}
knn = KNeighborsClassifier()
knn_cv = GridSearchCV(knn, param_grid, cv=5)
knn_cv.fit(X,Y)
knn_cv.best_params
knn_cv.best_score_

*Preprocessing data
-> A dummy variable is one that takes only the value 0 or 1 to indicate the absence or presence of some categorical effect that may be expected to shift the outcome. Dummy variables are useful because they enable us to use a single regression equation to represent multiple groups.

*Encoding dummy variables
import pandas as pd
df = pd.read_csv('auto.csv')
df_origin = pd.get_dummies(df)
print(df_origin.head())

df_origin = df_origin.drop('origin_Asia', axis=1)
print(df_origin.head())

*Imputing missig data
from sklearn.preprocessing import Imputer
imp = Imputer(missing_values='NaN', strategy='mean', axis=0)
imp.fit(X)
X = imp.transform(X)

*Imputing with a pipeline
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import Imputer
imp = Imputer(missing_values='NaN', strategy='mean', axis=0)
logreg = LogisticRegression()
steps = [('imputation',imp),('logistic_regression',logreg)]
pipeline = Pipeline(steps)
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
pipeline.fit(X_train, Y_train)
y_pred = pipeline.predict(X_test)
pipeline_score(X_test, Y_test)

*Scaling in a pipeline
from sklearn.preprocessing import StandardScaler
steps = [('scaler', StandardScaler()), ('knn', KNeighborClassifier())]
pipeline = Pipeline(steps)
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
knn_scaled = pipeline.fit(_train, Y_train)
Y_pred = pipeline.predict(X_test)
accuracy_score(Y_test, Y_pred)

*CV and Scaling in a pipeline
Steps = [('scaler', StandardScaler()), ('knn', KNeighborClassifier())]
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3, random_state = 42)
knn_scaled = pipeline.fit(_train, Y_train)
cv = GridSearchCV(pipeline, param_grid = parameters)
cv.fit(X_train, Y_train)
Y_pred = cv.predict(X_test)


**UNSUPERVISED LEARNING

-> It finds patterns in data.
Example : Clustering customers by their purchases and compressing the data using purchase patterns.

from sklearn.cluster import KMeans
model = KMeans(n_clusters = 3)
model.fit(samples)
labels = model.predict(samples)
print(labels)

-> Mean of each cluster : centroid

*Scatter plots
import matplotlib.pyplot as plt
xs = samples[:,0]
ys = samples[:,2]
plt.scatter(xs,ys,c=labels)
plt.show()

*Cross tabulation with pandas
*Aligning labels and species
import pandas as pd
df = pd.DataFrame({'labels':labels, 'species':species})
print(df)

*Crosstab of labels and species
ct = pd.crosstab(df['labels'], df['species'])
print(ct)

*Inertia measures cluster quality
-> Measures how spread out the clusters are(lower is better)
-> k-means attempts to minimize the inertia when choosing clusters

from sklearn.clusters import KMeans

model = KMeans(n_clusters = 3)
model.fit(samples)
print(model_inertia)

*sklearn StandardScaler
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
scaler.fit(samples)
StandardScaler(copy=True, with_mean=True, with_std = True)
sample_scaled = scaled.transform(samples)

-> For better clustering, first use StandardScaler and then KMeans. Use Sklearn pipeline to combine multiple steps.

*Pipelines combine multiple steps
from sklearn.preprocessing import StandardScaler
from sklearn.cluster import KMeans
scaler = StandardScaler()
model = KMeans(n_clusters = 3)
from sklearn.pipeline import make_pipeline
pipeline = make_pipeline(scaler, kmeans)
pipeline.fit(samples)
labels = pipeline.predict(samples)

-> StandardScaler is a "preprocessing" step.
-> Other Examples : MaxAbsScaler and Normalizer

*Hierarchical clustering with SciPy
import matplotlib.pyplot as plt
from scipy.cluster.hierarchy import linkage, dendrogram
mergings = linkage(samples, method = 'complete')
dendrogram(mergings, labels = country_names, leaf_rotation = 90, leaf_font_size = 6)
plt.show()

-> Distance between clusters is defined by a "linkage method"
-> In "complete" linkage : distance between clusters is max.

*Extracting the cluster labels
-> Use fcluster() function
-> Returns a NumPy array of cluster labels

from scipy.cluster.hierarchy import linkage
mergings = linkage(samples, method = 'complete')
from scipy.cluster.hierarchy import fcluster
labels = fcluster(mergings, 15, criterion='distance')
print(labels)

*t-SNE for 2-dimensional maps
t-SNE : "t-distributed stochastic neighbor embedding"
-> Maps sample to 2D space(or 3D)
-> Great for insoecting datasets

*t-SNE in sklearn
import matplotlib.pyplot as plt
from sklearn.manifold import TSNE
model = TSNE(learning_rate = 100)
transformed = model.fit_transform(samples)
xs = transformed[:,0]
ys = transformed[:,1]
plt.scatter(xs, ys, c=species)
plt.show()

-> t-SNE has only fit_transform() method
-> It simultaneously fits the model and transforms the data
-> Has no separate fit() or transform() method


*PCA : Principal Component Analysis
-> It is a fundamental dimension reduction technique.
-> PCA aligns data with axes by rotating
-> Shifts data sample so they have 0 mean
-> PCA is a scikit learn component
-> fit() learns the transformation from given data
-> transform() applies the learned transformation

from sklearn.decomposition import PCA
model = PCA()
model.fit(samples)
transformed = model.transform(samples)

*Pearson correlation
-> Measures linear correlation of features
-> Value between 1 and -1
-> 0 value means no linear correlation

import matplotlib.pyplot as plt
from scipy.stats import pearsonr
width = grains[:,0]
length = grains[:,1]
plt.scatter(width, length)
plt.axis('equal')
plt.show()
correlation, pvalue = pearsonr(width, length)
print(correlation)

*Intrinsic dimension
-> It is the number of features needed to approximate the dataset.
-> PCA identifies intrinsic dimension when samples have any number of features
-> Intrinsic dimension = number of PCA features with significant variance

*Plotting the variance of PCA features
import matplotlib.pyplot as plt
from sklearn.decomposition import PCA
pca = PCA()
pca.fit(samples)
features = range(pca.n_components_)
plt.bar(features, pca.explained_variance_)
plt.xticks(features)
plt.ylabel('variance')
plt.xlabel('PCA feature')
plt.show

*Sparse arrays and csr_matrix
-> "Sparse":most entries are zero
-> Can use scipy.sparse.csr_matrix instead of NumPy array
-> csr_matrix remembers only the non-zero entries

*TruncatedSVD and csr_matrix
-> scikit learn PCA doesn't support csr_matrix
-> use scikit-learn TruncatedSVD instead 
-> Performs same transformation

from sklearn.decomposition import TruncatedSVD
model = TruncatedSVD(n_components=3)
model.fit(documents)
TruncatedSVD(algorithm ='randomized',...)
transformed = model.transform(documents)

*Non-negative matrix factorisation(NMF)
-> Dimension reduction technique
-> NMF models are interpretable(unlike PCA)
-> All sample features are non-negative
-> Follows fit()/transform() pattern
-> Must specify no.of components
-> Works both with Numpy arrays and csr_matrix

from sklearn.decomposition import NMF
model = NMF(n_components = 2)
model.fit(samples)
nmf_features = model.transform(samples)

#Reconstruction of a sample
print(sample[i,:])

*Grayscale images
-> Has no colors, only shades of gray
-> Measures pixel brightness
Value between 0 and 1

*Visualizing samples
from matplotlib import pyplot as plt
plt.imshow(bitmap, cmap='gray', interpolation='nearest')
plt.show()

*Cosine similarities
-> Uses the angle between the lines
-> Higher values means more similiar

*Calculating cosine similarities
from sklearn.preprocessing import normalize
norm_features = normalize(nmf_features)
#if has index 23
current_article = norm_features[23,:]
similarities = norm_features.dot(current_article)
print(similarities)

*DataFrames and labels
import pandas as pd
norm_features = normalize(nmf_features)
df = pd.DataFrame(norm_features, index=titles)
current_article = df.loc['Dog bites man']
similarities = df.dot(current_article)
print(similarities.nlargest())




**CLASSIFICATION-TREE

-> Sequence of if-else questions about indivdual features.
-> Objective: infer class labels.
-> Capture non-linear relationship between features and labels.
-> Don't require feature scaling.

*Classification-tree in scikit-learn
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,stratify=Y,random_state=1)
dt = DecisionTreeClassifier(max_depth=2, random_state=1)
dt.fit(X_train, Y_train)
Y_pred = dt.predict(X_test)
accuracy_score(Y_test, Y_pred)

-> Decision regions : Region in the feature pace where all instances are assigned to one class label.
-> Decision boundary : surface separating different decision regions.
-> Decision Tree : Data structure consisting of a hierarchy of nodes.
-> Node : question or prediction.

-> Three kinds of nodes :
1) Root : no parent node, question giving rise to two children nodes.
2) Internal node : one parent node, question giving rise to two children nodes.
3) Leaf : one parent node, no children node. --> prediction

-> Nodes are grown recursively.
-> At each node, split the data based on:
* feature f and split-point sp to maximize IG(node) (IG : Information Gain)
-> If IG(node)= 0, declare the node a leaf.

*Information criterion in scikit-learn
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,stratify=Y,random_state=1)
dt = DecisionTreeClassifier(criterion="gini", random_state=1)
dt.fit(X_train, Y_train)
Y_pred = dt.predict(X_test)
accuracy_score(Y_test, Y_pred) (Accuracy increases)

*Decision-tree for regression
*Regression-tree in scikit-learn

from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error as MSE

X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=1)
dt = DecisionTreeClassifier(max_depth=4, min_samples_leaf=0.1, random_state=1)
dt.fit(X_train, Y_train)
Y_pred = dt.predict(X_test)
mse_dt = MSE(Y_test, Y_pred) (Obtain root mean square error of your model)
rmse_dt = mse_dt**(1/2)
print(rmse_dt)

*Generalization Error
Generalization error of f1 = bias^2 + variance + irreducible error
Bias : error term that tells you, on average, how much f1 not equal to f
Variance : tells how much f1 is inconsistent over different training sets.
Model complexity : sets the flexibility of f1.
Examples : max tree depth, min samples per leaf
Best model complexity = lowest generalization error

*Estimating the Generalization Error
-> split the data to training and test sets.
-> fit f1 to the training set.
-> evaluate the error of f1 on the unseen test set.
-> generalization error of f1 = test set error of f1

-> For better model Evaluation consider:
* Cross-Validation(CV)
-> K-Fold CV,
-> Hold-Out CV

CV error = (E1, E2, ..., E10)/10

-> Diagnose variance problems :
If f1 suffers from high variance: CV error of f1 > training set error of f1.
Thus, f1 has said to overfit the training set.
To remedy overfitting :
1) decrease model complexity
2) decrease max depth, increase min samples per leaf
3) gather more data..

-> Diagnose bias problems :
If f1 suffers from high bias: CV error of f1 = training set error of f1 >>> desired error
Thus, f1 has said to underfit the training set
To remedy underfitting :
1) increase model complexity
2) increase max depth, decrease min samples per leaf
3) gather more relevant features

*K-Fold CV in sklearn

from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error as MSE
from sklearn.model_selection import cross_val_score

SEED = 123
X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=SEED)
dt = DecisionTreeClassifier(max_depth=4, min_samples_leaf=0.1, random_state=SEED)
MSE_CV = - cross_val_score(dt, X_train, Y_train, cv=10, scoring='neg_mean_squared_error', n_jobs = -1)
dt.fit(X_train, Y_train)
Y_predict_train = dt.predict(X_train)
Y_predict_test = dt.predict(X_test)
print('CV MSE : {:,F}'.format(MSE_CV.mean())

*Ensemble Learning
It is the solution towrads the limitations of CARTS(Classification and Regression Trees)

-> Train different models on the ame dataset.
-> Let each model make its predictions.
-> Meta-model : aggregates predictions of individual models.
-> Final prediction : more robust and less prone to errors.

*Voting Classifier in sklearn

from sklearn.metrics import accuracy_score
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.neighbors import KNeighborslassifier as KNN
from sklearn.ensemble import VotingClassifier

SEED = 1
X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=SEED)
lr = logisticegression(random_state = SEED)
knn = KNN()
dt = DecisionTreeClassifier(random_state = SEED)

classifiers = [('Logistic Regression', lr), ('K Nearest Neighbour's, knn), ('Classification Tree', dt)]

for clf_name, clf in classifiers :
    clf.fit(X_train, Y_train)
    y_pred = clf.predict(X_test)
    print('{:s} : {:.3f}'.format(clf_name, accuracy_score(y_test, y_pred))
    
vc = VotingClassifier(estimators = classifiers)
vc.fit(X_train, X_test)
y_pred = vc.predict(X_test)
print('Voting Classifier : {.3f}'.format(accuracy_score(y_test, y_pred)))
    


**BAGGING

-> Bootstrap aggregration
-> Uses a technique known as bootstrap
-> Reduces variance of individual models in ensemble

*Classification :
-> Aggregates prediction by majority voting
-> BaggingClassifier in scikit-learn

*Regression :
-> Aggreagates prediction through averaging
-> BaggingRegressor in scikit-learn

from sklearn.ensemble import BaggingClassifier
from sklearn.metrics import accuracy_score
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier

SEED = 1
X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=SEED)
dt = DecisionTreeClassifier(max_depth=4, min_samples_leaf=0.16, random_state = SEED)
bc = BaggingClassifier(base_estimator=dt, n_estimators=300, n_jobs=-1)
bc.fit(X_train, Y_train)
y_pred = bc.predict(X_test)
accuracy = accuracy_score(Y_test, Y_pred)
print('Accuracy of Bagging Classifier : {:.3f}'.format(accuracy))

-> On average, for each model, 63% of the training instances are sampled.
-> The remaining 37% constitute the OOB(Out of Bag) instances.

from sklearn.ensemble import BaggingClassifier
from sklearn.metrics import accuracy_score
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier

SEED = 1
X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=SEED)
dt = DecisionTreeClassifier(max_depth=4, min_samples_leaf=0.16, random_state = SEED)
bc = BaggingClassifier(base_estimator=dt, n_estimators=300,oob_score = True, n_jobs=-1)
bc.fit(X_train, Y_train)
y_pred = bc.predict(X_test)
test_accuracy = accuracy_score(Y_test, Y_pred)
oob_accuracy = bc.oob_score_
print('Test set accuracy: {:.3f}'.format(test_accuracy))
print('OOB accuracy: {:.3f}'.format(oob_accuracy))

-> In bagging, Base estimator : Decision Tree, Logistic Regression, Neural Net..
-> Estimators use all features for training and prediction

*Random Forest(RF)
-> Base estimator : Decision Tree
-> RF introduces further randomization in the training of individual trees.
-> d features are sampled at each node without replacement
(d < total number of features)

*Classification :
-> Aggregates prediction by majority voting
-> RandomForestClassifier in scikit-learn

*Regression :
-> Aggreagates prediction through averaging
-> RandomForestRegressor in scikit-learn

from sklearn.ensemble import RandomForestRegressor
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error as MSE

SEED = 1
X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=SEED)
rf = RandomForestRegressor(min_samples_leaf=0.12, n_estimators=300, random_state = SEED)
rf.fit(X_train, Y_train)
y_pred = rf.predict(X_test)
rmse_test = MSE(Y_test, Y_pred) ** (1/2)
print('Test set RMSE of rf: {:.2f}'.format(rmse_test))

*Feature Importance :
-> Tree-based methods: enable measuring the importance of each feature in prediction
-> In sklearn :
* how much the tree nodes use a particular feature(weighted average) to reduce impurity
* accessed using the attribute feature_importance

import pandas as pd
import matplotlib.pyplot as plt

importances_rf = pd.Series(rf.feature_importance_, index = X.columns)
sorted_importances_rf = importances_rf.sort_values()
sorted_importances_rf.plot(kind='barh', color='lightgreen')
plt.show()




**ADABOOST

-> Boosting : Ensemble method combining several weak learners to form a strong learner.
-> Weak learner : Model doing slightly bettwer than random guessing.
-> Most popular boosting methods :
* AdaBoost
* Gradient Boosting

*Adaboost
-> Stands for Adaptive Boosting
-> Each predictor pays more attention to the instances wrongly predicted by its predecessor
-> Achieved by changing the weights of training instances
-> Each predictor is assigned a coefficient alpha
-> alpha depends on the predictor's training error

*Adaboost in sklearn

from sklearn.ensemble import AdaBoostClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import roc_auc_score
from sklearn.tree import DecisionTreeClassifier

SEED = 1
X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=SEED)
dt = DecisionTreeCassifier(max_depth=1, random_state=SEED)
adb_clf = AdaBoostClassifier(base_estimator=dt, n_estimators=100)
adb_clf.fit(X_train, Y_train)
Y_pred_proba = adb_clf.predict_proba(X_test)[:,1]
adb_clf_roc_auc_score = roc_auc_score(Y_test, Y_pred_proba)
print('ROC AUC score: {:.2f}'.format(adb_clf_roc_auc_score))

*Gradient Boosting(GB)
-> Sequential correction of predecessor's error.
-> Does not tweak the weights of training instances.
-> Fit each predictor is trained using its predecessor's residual errors as labels.
-> Gradient Boost Trees : a CART is used as a base learner

*Gradient Boosting in sklearn

from sklearn.ensemble import GradientBoostRegressor
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error as MSE

SEED = 1
X_train, X_test, Y_train, Y_test = train_test_split(X,Y,test_size=0.2,random_state=SEED)
gbt = GradientBoostRegressor(n_estimators=300, max_depth=1, SEED)
gbt.fit(X_train, Y_train)
Y_pred = g

*Stochastic Gradient Boosting(SGB)
-> Each tree is trained on a random subset of rows of the training data.
-> The sampled instances(40%-80% of training sets) re sampled without replacement.
-> Features are sampled when choosing split points.
-> Result : further ensemble diversity
-> Effect : adding further variance to the ensemble of trees

*Stochastic Gradient Boosting in sklearn

from sklearn.ensemble import GradientBoostRegressor
from sklearn.mod

sgbt = GradientBoostRegressor(max_depth=1, subsample=0.8, max_features=0.2, n_estimators=300, SEED)
sgbt.fit(X_train, Y_train)
Y_pred = sgbt.predict(X_test)
rmse_test = MSE(Y_test, Y_pred) ** (1/2)
print('Test set RMSE: {:.2f}'.format(rmse_test))



**TUNING A CART'S HYPERPARAMETERS

*Hyperparameters
*parameters : learned from data
-> CART example : split-point of node, split-feature of a node etc
*hyperparameters : not learned from data, set prior to training
-> CART example : max_depth, min_samples_leaf, splitting criterion

-> optimal model : yields an optimal score
-> score : in sklearn defaults to accuracy(classification) and R^2(regression)
-> Cross validation is used to estimate the generalization performance

*Approaches to hyperparameter tuning :
-> Grid Search
-> Random Search
-> Bayesian Optimization
-> Genetic Algorithms

from sklearn.model_selection import GridSearchCV
params_dt = {'max_depth': [1, 2, 3, 4]
             'min_samples_leaf': [0.02, 0.03, 0.04, 0.09]
             'max_features': [0.2, 0.4, 0.6, 0.9]}

grid_dt = GridSerachCV(estimator = dt, param_grid = params_cv, scoring = 'accuracy', cv = 10, n_jobs = -1)
grid_dt.fit(X_train, Y_train)
best_hyperparams = grid_dt.best_params_
print('Best hyperparameters:\n', best_hyperparams)
best_model = grid_dt.best_estimator_

*Random Forests Hyperparameters
-> CART hyperparameters
-> number of estimators
-> bootstrap

-> Hyperparameter tuning is sometimes expensive and leads to very slight improvement at times.

*Inspecting RF Hyperparameters in sklearn
from sklearn.ensemble import RandomForestRegressor
SEED = 1
rf = RandomForestRegressor(random_state = SEED)
rf.get_params()


**UNSUPERVISED LEARNING

Common unspervised learning algorithms : clustering, neural networks, nomaly detection
-> Clustering : The process of grouping items with similiar characteristics.

*Plotting data for clustering
 from matplotlib import pyplot as plt
 x_coordinates = [89, 90, 65, 67, 33, 60]
 y_coordinates = [22, 78, 89, 90, 80, 44]
 plt.scatter(x_coordinates, y_coordinates)
 plt.show()
 
 *Hierarchial clustering in SciPy
 from scipy.cluster.hierarchy import linkage, fcluster
 from matplotlib import pyplot as plt
 import seaborn as sns, pandas as pd
 
 x_coordinates = [89, 90, 65, 67, 33, 60]
 y_coordinates = [22, 78, 89, 90, 80, 44]
 
 df = pd.DataFrame({'x_coordinate' : x_coordinates, 'y_coordinate' : y coordinates})
 
 Z = linkage(df, 'ward')
 df['cluster_labels'] = fcluster(Z, 3, criterion='maxclust')
 sns.scatterplot(x='x_coordinate', y='y_coordinate', hue='cluster_labels', data = df)
 plt.show()
 
 
 *K-means clustering in scipy
 from scipy.cluster.vq import kmeans, vq
 from matplotlib import pyplot as plt
 import seaborn as sns, pandas as pd
 
 import random
 random.seed((1000,2000))
 
 x_coordinates = [89, 90, 65, 67, 33, 60]
 y_coordinates = [22, 78, 89, 90, 80, 44]
 
 df = pd.DataFrame({'x_coordinate' : x_coordinates, 'y_coordinate' : y coordinates})
 
 centroids,_ = kmeans(df, 3)
 df['cluster_labels'], _ = vq(df, centroids)
 
 *Normalization of data
 -> Process of rescaling data to a standard deviation of 1
 x_new = x / std_dev(x)
 
 from matplotlib import pyplot as plt
 plt.plot(data, label = "original")
 plt.plot(scaled_data, label = "scaled")
 
 plt.legend()
 plt.show()
 
 *Standardize data using whiten() function
 from scipy.cluster.vq import whiten
 
 goals_for = [2, 4, 6, 7, 8, 9]
 scaled_data = whiten(goals_for)
 print(scaled_data)
 
 
 *Creating a distance matrix using linkage
 scipy.cluster.hierarchy.linkage(observations, method='single', metric='euclidean', optimal_ordering=False)
 
 method : how to calculate the proximity of clusters
 metric : distance metric
 optimal_ordering : order data points
 
 Which method to use ?
 -> single : based on two closest objects
 -> complete : based on two farthest objects
 -> average : based on the arithmetic mean of all objects
 -> centroid : based on the geometric mean of all objects
 -> median : based on the median of all objects
 -> ward : based on the sum of squares
 
 *Creating cluster labels with fcluster
 scipy.cluster.hierarchy.fcluster(distance_matrix, num_clusters, criterion)
 
 distance_matrix : output of linkage() method
 num_clusters : number of clusters
 criterion : how to decide thresholds to form clusters
 
 *Visualize clusters with matplotlib
 from matplotlib import pyplot as plt
 
 df = pd.DataFrame({'x': [2, 4, 5, 6, 7], 'y': [1, 1, 4, 5, 6], 'labels': ['A', 'B', 'A', 'A', 'B']})
 df.plot.scatter(x='x', y='y', c=df['labels'].apply(lambda x: colors[x])
 plt.show()
 
 *Visualize clusters with seaborn
 from matplotlib import pyplot as plt
 import seaborn as sns
 
 df = pd.DataFrame({'x': [2, 4, 5, 6, 7], 'y': [1, 1, 4, 5, 6], 'labels': ['A', 'B', 'A', 'A', 'B']})
 sns.scatterplot(x='x', y='y', hue='labels', data=df)
 plt.show()
 
 *Create a dendrogram in SciPy
 from scipy.cluster.hierarchy import dendrogram
 
 Z = linkage(df[['x_whiten', 'y_whiten']], method = 'ward', metric = 'euclidean')
 dn = dendrogram(Z)
 plt.show()
 
 *Measuring speed in hierarchial clustering
 -> timeit module to check runtime of functions
 -> Measure the speed of .linkage() method
 -> Use randomly generated points
 -> Run various iterations to extrapolate
 
 *Use of timeit module
 from scipy.cluster.hierarchy import linkage
 import pandas as pd
 import random, timeit
 
 points = 100
 df = pd.DataFrame({'x': random.sample(range(0, points), points), 'y': random.sample(range(0, points), points)})
 %timeit linkage(df[['x', 'y']], method = 'ward', metric = 'euclidean')
 
 *K-means clustering
 
 Drawback of hierarchial clustering : runtime
 -> k means runs significantly faster on large datasets
 
 *STEP-1 : Generate cluster centers
 kmeans(obs, k_or_guess, iter, thresh, check_finite)
 obs : standardized observations
 k_or_guess : number of clusters
 iter : number of iterations(default : 20)
 thres : threshold(default : 1e-05)
 check_finite : whether to check if observations contain only finite numbers(default=True)
 -> Returns two objects : cluster centers, distortion
 
 *STEP-2: Generate cluster labels
 vq(obs, code_book, check_finite=True)
 obs : standardized observations
 code_book : cluster centers
 check_finite : whether to check if observations contain only finite numbers(default=True)
 -> Returns two objects : a list of cluster labels, a list of distortions
 
 -> k-means returns a single value of distortions
 -> vq(Vector quantization) returns a list of distortions
 
 *Running k-means
 from scipy.cluster.vq import kmeans, vq
 
 cluster_centers,_ = kmeans(df[['scaled_x', 'scaled_y']],3)
 df['cluster_labels'],_ = vq(df[['scaled_x', 'scaled_y']],cluster_centers)
 
 sns.scatterplot(x='scaled_x', y='scaled_y', hue='cluster_labels', data=df)
 plt.show()
 
 -> Distortion : sum of squared distances of points from cluster centers
 -> Decreases with an increasing number of clusters
 -> Becomes zero hen the number of clusters equals the number of points
 -> Elbow plot : line plot between cluster centers and distortion
 -> It helps to indicate the number of clusters present in data
 
 *Elbow method in Python
 distortions = []
 num_clusters = range(2,7)
 
 for i in num_clusters:
     centroids, distortions = kmeans(df[['scaled_x', 'scaled_y']], i)
     distortions.append(distortion)
     
 elbow_plot_data = pd.DataFrame({'num_clusters': num_clusters, 'distortions': distortion})
 sns.lineplot(x='num_clusters', y='distortions', data = elbow_plot_data)
 plt.show()
 
 *Dominent colors in Images
 -> All images consist of pixels
 -> Each pixel has three values : Red, Green and Blue
 -> Pixel color : combination of these RGB values
 -> Perform k-means on standardized RGB to find cluster centers
 -> Uses : identifying features in satellite images
 
 -> Convert images to pixels : matplotlib.image.imread
 -> Display colors of cluster centers : matplotlib.pyplot.imshow
 
 *Convert image to RGB matrix
 import matplotlib.image as img
 mage = img.imread('sea.jpg')
 image.shape
 
 r=[]
 g=[]
 b=[]
 
 for row in image:
     for pixel in row:
         temp_r, temp_g, temp_b = pixel
         r.append(temp_r)
         g.append(temp_g)
         b.append(temp_b)
         
         
*Find dominant colors
cluster_centers,_ = kmeans(pixels[['scaled_red', 'scaled_blue', 'scaled_green']],2)

colors = []

r_std, g_std, b_std = pixels[['red', 'blue', 'green']].std()

for cluster_center in cluster_centers :
    scaled_r, scaled_g, scaled_b = cluster_centers
    colors.append((scaled_r * r_std/255, scaled_g * g_std/255, scaled_b * b_std/255))
  
print(colors)
plt.imshow([colors])
plt.show()


    


***DEEP LEARNDING IN PYTHON

-> Deep learning uses especially powerful neural networks.
-> A neural network is a series of algorithms that endeavors to recognize underlying relationships in a set of data through a process that mimics the way the human brain operates.
-> A simple neural network has an input layer, hidden layer and output layer.

-> Forward Propogation: Multiply-add process.
                        Dot product.
                        Forward propogation for one data point at at time.
                        Output is the prediction for that data point.
                        
-> Forward Propogation code:
import numpy as np
input_data = np.array([2,3])
weights = {'node_0': np.array([1, 1]), 'node_1': np.array([-1, 1]), 'output': np.array([2, -1])}
node_0_value = (input_data * weights['node_0']).sum()
node_1_value = (input_data * weights['node_1']).sum()
hidden_layer_outputs = np.array([node_0_value, node_1_value])
output = (hidden_layer_outputs * weights['output']).sum()
print(output)

-> Activation function allows the model to capture non-linearities.
-> Activation functions applied to node inputs to produce node outputs.

->The rectified linear activation function or ReLU for short is a piecewise linear function that will output the input directly if it is positive, otherwise, it will output zero.

-> Activation function code:
import numpy as np
input_data = np.array([2,3])
weights = {'node_0': np.array([1, 1]), 'node_1': np.array([-1, 1]), 'output': np.array([2, -1])}
node_0_input = (input_data * weights['node_0']).sum()
node_0_output = np.tanh(node_0_input) (can also use relu instead of np.tanh)
node_1_input = (input_data * weights['node_1']).sum()
node_1_output = np.tanh(node_1_input)
hidden_layer_outputs = np.array([node_0_value, node_1_value])
output = (hidden_layer_outputs * weights['output']).sum()
print(output)


*The need for optimization
-> making accurate predictions get harder with more points.

-> Loss function: Aggregates errors in predictions from many data points into single number.
-> Measure of model's predictive performance.
-> Lower loss function value means a better model.
-> Use algorithm called Gradient descent.

-> Gradient descent is a first-order iterative optimization algorithm for finding a local minimum of a differentiable function.

*Gradient descent steps
-> Start at random point
-> Until you are somewhere flat:
  - Find the slope
  - Take a step downhill

-> If the slope is positive-
  - Going opposite the slope means moving to lower numbers
  - Subtract the slope from the current value
  - Too big a step may lead us astray

-> Solution : learning rate
-> Update each weight by subtracting learning rate * slope

-> Slope calculation example
<img width="624" alt="Screen Shot 2021-03-10 at 7 41 28 PM" src="https://user-images.githubusercontent.com/77609240/110722836-9f45c180-81d8-11eb-8f82-aeb156df0fcc.png">

-> Slope of mean-squared loss function w.r.t prediction:
   -> 2(Predicted Value - Actual Value) = 2 Error
   -> 2(-4) = -8
   
 -> Slope of loss:
    -> 2 * -4 * 3 = -24
    -> learning rate = 0.01
    -> Updated weight = 2 - 0.01(-24) = 2.24
    
 
-> Code to calculate slopes and update weights:
import umpy as np
weights = np.array([1,2])
input_data = np.array([3,4])
target = 6
learning_rate = 0.01
preds = (weights * input_data).sum()
error = preds - target
print(error)

gradient = 2 * input_data * error
gradient

weights_updated = weights - learning_rate * gradient
preds = (weights * input_data).sum()
error_updated = preds_updated - target
print(error_updated)

-> Backpropagation is a short form for "backward propagation of errors." It is a standard method of training artificial neural networks. This method helps to calculate the gradient of a loss function with respects to all the weights in the network.

-> Backpropogation process:
- Trying to estimate the slope of the loss function w.r.t each weight.
- Do forward propogation to alculate predictions and errors.
- Go back one layer at a time.
- Gradients for weight is product of:
  1. Node value feeding into that weight.
  2. Slope of loss function w.r.t node it feeds into.
  3. Slope of activation function at the node it feeds into.

-> Backpropogation: Recap
- Start at some random set of weights.
- Use forward propogation to make a prediction.
- Use backward propogation to calculate the slope of the loss function w.r.t each weight.
- Multiply that slope by the learning rate, and subtract from the urrent weights.
- Keep going with the cycle until we get to a flat part.

-> Stochastic gradient descent: Stochastic gradient descent is an iterative method for optimizing an objective function with suitable smoothness properties. Advantages of using Stochastic Gradient Descent is that it does the calculations faster than gradient descent and batch gradient descent. However, gradient descent is the best approach if one wants a speedier result.
   
-> It is common to calculate slopes on only a subset of the data.
-> Use a different batch of data to calculate the next update.
-> Start over from the beginning once all data is used.
-> Each time through the training data is called an epoch.
-> When slopes are calculated on one batch at a time: stochastic gradient descent



**CREATING A KERAS MODEL

-> Model building steps:
  - Specify architecture
  - Compile
  - Fit
  - Predict

-> Model specification:
import numpy as np
from keras.layers import Dense
from keras.models import Sequential

predictors = np.loadtxt('predictors_data.csv', delimiter=',')
n_cols = predictors.shape[1]

model = Sequential()
model.add(Dense(100, activation='relu', input_shape = (n_cols,)))
model.add(Dense(100, activation='relu'))
model.add(Dense(1))

-> Why you need to compile your model?
- Specify the optimizer
  1. Many options and mathematically complex
  2. "Adam" is usually a good choice
- Loss function
  1. "mean_squared_error" common for regression

Example:
predictors = np.loadtxt('predictors_data.csv', delimiter=',')
n_cols = predictors.shape[1]

model = Sequential()
model.add(Dense(100, activation='relu', input_shape = (n_cols,)))
model.add(Dense(100, activation='relu'))
model.add(Dense(1))
model.compile(optimizer='adam', loss='mean_squared_error')

-> Fitting a model
- Applying backpropogation and gradient descent with your data to update the weights.
- Scaling data before fitting can ease optimization.

Example:
predictors = np.loadtxt('predictors_data.csv', delimiter=',')
n_cols = predictors.shape[1]

model = Sequential()
model.add(Dense(100, activation='relu', input_shape = (n_cols,)))
model.add(Dense(100, activation='relu'))
model.add(Dense(1))
model.compile(optimizer='adam', loss='mean_squared_error')
mpdel.fit(predictors, target)


**Classification models

-> 'categorical_crossentropy' loss function
-> Similiar to log loss
-> Add metrics = ['accuracy'] to compile step for easy-to-understand diagnostics.
-> Output layer has separate node for each possible outcome, and uses 'softmax' activation.

-> Code for Classification model:
from keras.utils.np_utils import to_categorical

data = pd.read_csv('basketball_shot_log.csv')
predictors = data.drop(['shot_result'], axis=1).as_matrix()
target = to_categorical(data.shot_result)

model = Sequential()
model.add(Dense(100, activation='relu', input_shape = (n_cols,)))
model.add(Dense(100, activation='relu')
model.add(Dense(100, activation='relu')
model.add(Dense(2, activation='softmax')
model.compile(optimizer = 'adam', loss ='categorical_crossentropy', metrics = ['accuracy'])
model.fit(predictors, target)

-> Using models:
1. Save
2. Reload
3. Make predictions

Example:
from keras.models import load_model
model.save('model_file.h5')
my_model = my_model.predict(data_to_predict_with)
probability_true = predictions[:,1]

Verifying modle structure : my_model.summary()


-> Vanishing gradients: occurs when many layers have very small slopes(e.g due to being on flat part of tanh curve)
-> In deep networks, updates to backprop were close to 0.

*Validation in deep learning
-> Commonly use validation split rather than cross-validation.
-> Deep learning widely used on large datasets.
-> Single validation score is based on large amount of data, and is reliable.

-> Example of model validation:
model.compile(optimizer = 'adam', loss = 'categorical_crossentropy', metrics = ['accuracy'])
model.fit(predictors, target, validation_split = 0.3)

**Early Stopping

-> Early stopping is a method that allows you to specify an arbitrary large number of training epochs and stop training once the model performance stops improving on a hold out validation dataset.

from keras.callbacks import EarlyStopping
early_stopping_monitor = EarlyStopping(patience = 2)
model.fit(predictors, target, validation_split = 0.3, nb_epoch = 20, callbacks = [early_stopping_monitor])


-> Overfitting is a modeling error which occurs when a function is too closely fit to a limited set of data points. Underfitting refers to a model that can neither model the training data nor generalize to new data. Intuitively, underfitting occurs when the model or the algorithm does not fit the data well enough.

-> Workflow for optimizing model capacity:
1. Start with a small network.
2. Gradually increase capacity.
3. Keep increasing capacity until validation score is no longer improving.




**INTRODUCTION TO TENSORFLOW IN PYTHON

-> Tensorflow is an open-source library for graph-based numerical computation.
-> Used for addition, multiplication, differentiation, train machine learning models.

-> Tensor is a generalization of vectors and matrices.
-> A collection of numbers arranged in a particular shape.

-> Defining tensors in TensorFlow
   import tensorflow as tf
   
   d0 = tf.ones((1,)) #O-dimension tensor
   d1 = tf.ones((2,))
   d2 = tf.ones((2, 2))
   d3 = tf.ones((2, 2, 2))
   
   print(d3.numpy())
   
-> A constant is the simplest category of tensor.
-> Not trainable, can have only one dimension.

  from tensorflow import constant
  
  a = constant(3, shape=[2,3])  #define a 2x3 constant
  
  b = constant([1,2,3,4], shape=[2,2]) #define a 2x2 constant
  
-> Defining and initializing variables

   import tensorflow as tf
   
   #Define a variable
   a0 = tf.Variable([1,2,3,4,5,6], dtype=tf.float32)
   a1 = tf.Variable([1,2,3,4,5,6], dtype=tf.int16)
   
   #Define a constant
   b = tf.constant(2, tf.float32)
   
   #Compute their product
   c0 = tf.multiply(a0,b)
   c1 = a0*b
   
   
*Basic operations

-> Addition operation

from tensorflow import constant, add

#define 0-dimensional tensors
A0 = constant([1])
B0 = constant([1])

#define 1-dimensional tensors
A1 = constant([1, 2])
B1 = constant([3, 4])

#define 2-dimensional tensors
A2 = constant([1, 2], [3, 4])
B2 = constant([5, 6], [7, 8])

#Perform tensor addition with add()
C0 = add(A0, B0)
C1 = add(A1, B1)
C2 = add(A2, B2)

-> The add() operation performs element-wise addition with two tensors.
-> Element-wise addition requires both tensors to have the same shape.

-> Element-wise multiplication performed using multiply() operation.
-> Matrix multiplication performed with matmul() operator.
-> The matmul(A,B) operation multiplies A by B.
-> Number of columns of A must be equal to number of rows of B.

-> Multiplication operation

from tensorflow import ones, matmul, multiply

#define tensors
A0 = ones(1)
A31 = ones([3, 1])
A34 = ones([3, 4])
A43 = ones([4, 3])

- Valid operations:
1. multiply(A0,A0)
2. multiply(A31,A31)
3. multiply(A43,A43)
4. matmul(A43,A34)
5. not valid: matmul(A43,A43)

-> Summing over tensor dimensions
- The reduce_sum() operator sums over the dimensions of a tensor.
- reduce_sum(A) sums over all dimensions of A
- reduce_sum(A, i) sums over dimension i

from tensorflow import ones, reduce_sum

#define a 2x3x4 tensor of ones
A = ones([2,3,4])

#sum over all dimensions
B = reduce_sum(A)

#Sum over dimensions 0, 1 and 2
B0 = reduce_sum(A, 0)
B1 = reduce_sum(A, 1)
B2 = reduce_sum(A, 2)

*Advanced operations

-> gradient(): computes the slope of a function at a point
-> reshape(): reshapes a tensor(e.g 10x10 to 100x1)
-> random(): generates a tensor out of randomly drawn values

-> Finding the optimum:
1. Minimum: Lowest value of a loss function.
2. Maximum: Highest value of objective function.
-> Do this using gradient() operation
1. Optimum: Find a point where gradient = 0.
2. Minimum: Change in gradient > 0.
3. Maximum: Change in gradient < 0.

-> Gradients in TensorFlow

import tensorflow as tf

#Define x
x = tf.Variable(-1.0)

#Define y within instance of GradientTape
with tf.GradientTape() as tape:
     tape.watch(x)
     y = tf.multiply(x, x)
     
#Evaluate the gradient of y at x = -1
g = tape.gradient(y, x)
print(g.numpy())

-> How to reshape a grayscale image

import tensorflow as tf

#generate grayscale image
gray = tf.random.uniform([2,2], maxval = 255, dtype='int32')

#Reshape grayscale image
gray = tf.reshape(gray, [2*2, 1])

-> how to reshape a color image

import tensorflow as tf

#generate color image
color = tf.random.uniform([2,2,3], maxval = 255, dtype='int32')

#Reshape color image
color = tf.reshape(color, [2*2, 3])



*Importing data for use in tensorflow

-> Import data using pandas
-> Convert data to numpy array
-> Use in tensorflow without modification

import numpy as np
import pandas as pd

housing = pd.read_csv('kc_housing.csv')
housing = np.array(housing)


-> Parameters of read_csv()
   
   Parameter                  Description                             Default
1. filepath_or_buffer      Accepts a file path or URL                  None
2. sep                     Delimiter between columns                    ,
3. delim_whitespace        Boolean for whether to delimit whitespace   False
4. encoding                Specifies encoding to be used if any        None

-> Setting the data type using numpy and tensorflow approach

1. housing = pd.read_csv('kc_housing.csv')
   price = np.array(housing['price'], np.float32)
   waterfront = np.array(housing['waterfront'], np.bool)
   
2. housing = pd.read_csv('kc_housing.csv')
   price = tf.cast(housing['price'], tf.float32)
   waterfront = tf.cast(housing['waterfront'], tf.bool)
   
 *LOSS FUNCTIONS
 
 -> TensorFlow has operations for common loss functions
 1. Mean squared error(MSE)
 2. Mean absolute error(MAE)
 3. Huber error
 -> Loss functions are accesible from:
 1. tf.keras.losses()
 2. tf.keras.losses.mse()
 3. tf.keras.losses.mae()
 4. tf.keras.losses.Huber()
 
-> MSE
 - Strongly penalizes outliers
 - High sensitivity near minimum

-> MAE
 - Scales linearly with size of error
 - Low sensitivity near minimum

-> Huber
 - Similiar to MSE near minimum
 - Similiar to MAE away from minimum

import tensorflow as tf

loss = tf.keras.losses.mse(targets, predictions)

-> Defining a loss function

#Define a linear regression model
def linear_regression(intercept, slope = slope, features = features):
    return intercept + features*slope
    
#Define a loss function to compute the MSE
def loss_function(intercept, slope, targets = targets, features = features):
    predictions = linear_regression(intercept, slope)
    return tf.keras.losses.mse(target, predictions)
    
#Compute the loss for test data inputs
loss_function(intercept, slope, test_targets, test_features)

#Compute the loss for default data inputs
loss_function(intercept, slope)


*LINEAR REGRESSION in TenserFlow

price = np.array(housing['price'], np.float32)
size = np.array(housing['sqft_living'], np.float32)

intercept = tf.Variable(0.1, np.float32)
slope = tf.Variable(0.1, np.float32)

def linear_regression(intercept, slope = slope, features = size):
    return intercept + features*slope
    
def loss_function(intercept, slope, targets = price, features = size):
    predictions = linear_regression(intercept, slope)
    return tf.keras.losses.mse(target, predictions)
    
#define an optimization operation
opt = tf.keras.optimizers.Adam()

#Minimize the loss function and print the loss
for j in range(1000):
    opt.minimize(lambda: loss_function(intercept, slope), var_list = [intercept, slope])
    print(loss_function(intercept, slope))
    
#Print the trained parameters
print(intercept.numpy(), slope.numpy())


*Batch training

-> 'chunksize' parameter provides batch size

import pandas as pd
import numpy as np

for batch in pd.read_csv('kc_housing.csv', chunksize = 100)
    price = np.array(batch['price'], np.float32)
    size = np.array(batch['size'], np.float32)
    
-> Training a linear model in batches 

import pandas as pd
import numpy as np
import tensorflow as tf

intercept = tf.Variable(0.1, tf.float32)
slope = tf.Variable(0.1, tf.float32)

def linear_regression(intercept, slope, features):
    return intercept + features*slope
    
def loss_function(intercept, slope, targets, features):
    predictions = linear_regression(intercept, slope)
    return tf.keras.losses.mse(target, predictions)
    
opt = tf.keras.optimizers.Adam() 

for batch in pd.read_csv('kc_housing.csv', chunksize = 100)
    price_batch = np.array(batch['price'], np.float32)
    size_batch = np.array(batch['size'], np.float32)
    
opt.minimize(lambda: loss_function(intercept, slope), var_list = [intercept, slope])
print(intercept.numpy(), slope.numpy())



*DENSE LAYERS
-> A dense layer applies weights to all nodes from the previous layer.
 
  import tenserflow as tf
  
  #define inputs(features)
  inputs = tf.constant([[1, 35]])
  
  #define weights
  weights = tf.Variable([[-0.05],[-0.01]])
  
  #define bias
  bias = tf.Variable([0.5])
  
  #multiply inputs by the weights
  product = tf.matmul(inputs, weights)
  
  #define dense layer
  dense = tf.keras.activations.sigmoid(product+bias)
  
-> Defining a complete model
  
  import tensorflow as tf
  
  #define input layer
  inputs = tf.constant(data, tf.float32)
  
  #define first dense layer
  dense1 = tf.keras.layers.Dense(10, activation='sigmoid')(inputs)
  
  #define second dense layer
  dense2 = tf.keras.layers.Dense(5, activation='sigmoid')(dense1)
  
  #define output(predictions) layer
  outputs = tf.keras.layers.Dense(1, activation='sigmoid')(dense2)
  
  -> High-level approach
     - high-level API operations
     - dense = keras.layers.Dense(10, activation='sigmoid')

  -> Low-level approach
     - Linear-algebraic operations
     - prod = matmul(inputs, weights)
     - dense = keras.activations.sigmoid(prod)


-> Compenents of a typical hidden layer:
   - Linear: Matrix Multiplication
   - Nonlinear: Activation function

-> Sigmoid activation function
   - Primarily, used in outputs of binary classification.
   - Low-level: tf.keras.activations.sigmoid()
   - High-level: sigmoid

-> The relu activation function
   - Used for hidden layers.
   - Low-level: tf.keras.activations.relu()
   - High-level: relu

-> The softmax activation function
   - Used in output layers in classification problems having more than 2 classes.
   - Low-level: tf.keras.activations.softmax()
   - High-level: softmax

*Activation functions in neural networks

import tensorflow as tf

#define input layer
inputs = tf.constant(borrower_features, tf.float32)

#define dense layer 1
dense1 = tf.keras.layers.Dense(16, activation='relu')(inputs)

#define dense layer 2
dense1 = tf.keras.layers.Dense(8, activation='sigmoid')(dense1)

#define output layer
output = tf.keras.layers.Dense(4, activation='softmax')(dense2)

*Optimizers

-> The gradient descent optimizer
  - Stochastic gradient descent(SGD) optimizer
  - tf.keras.optimizers.SGD()
  - learning_rate
  - simple and easy to interpret

-> The RMS propogation optimizer
  - Root mean squared propogration optimizer
  - tf.keras.optimizers.RMSprop()
  - learning_rate
  - momentum
  - decay
  - Allows for momentum to both build and decay

-> The adam optimizer
  - Adaptive moment(adam) optimizer
  - tf.keras.optimizers.Adam()
  - learning_rate
  - beta1
  - Performs well with default parameter values

*Initialising variables in TensorFlow

-> Low-level approach

  import tensorflow as tf
  
  #define 500x500 random normal variable
  weights = tf.Variable(tf.random.normal([500, 500]))
  
  #define 500x500 truncated random normal variable
  weights = tf.Variable(tf.random.truncated_normal([500, 500]))
  
  
-> High-level approach

   #define a dense layer with the default initializer
   dense = tf.keras.layers.Dense(32, activation='relu')
   
   #define a dense layer with the zeros initializer
   dense = tf.keras.layers.Dense(32, activation='relu', kernel_initializer='zeros')
   
*Implementing dropout in a network

   import numpy as np
   import tensorflow as tf
   
   #define input data
   inputs = np.array(borrower_features, np.float32)
   
   #define dense layer 1
   dense1 = tf.keras.layers.Dense(32, activation='relu')(inputs)
   
   #define dense layer 2
   dense2 = tf.keras.layers.Dense(16, activation='relu')(dense1)
   
   #Apply dropout operation
   dropout1 = tf.keras.layers.Dropout(0.25)(dense2)
   
   #define output layer
   outputs = tf.keras.layers.Dense(1, activation='sigmoid')(dropout1)
   
   

*Building a sequential model

from tensorflow import keras

model = keras.Sequential()

#define first hidden layer
model.add(keras.layers.Dense(16, activation='relu', input_shape=(28*28)))

#define second hidden layer
model.add(keras.layers.Dense(8, activation='relu')

#define output layer
model.add(keras.layers.Dense(4, activation='softmax')

#compile the model
model.compile('adam', loss='categorical_crossentropy')

#summarize the model
print(model.summary())


*Building a functional API

import tensorflow as tf

#define model 1 input layer shape
model1_inputs = tf.keras.Input(shape=(28*28,))

#define model 2 input layer shape
model2_inputs = tf.keras.Input(shape=(10,))

#define layer 1 for model 1
model1_layer1 = tf.keras.layers.Dense(12, activation='relu')(model1_inputs)

#define layer 2 for model 1
model1_layer2 = tf.keras.layers.Dense(4, activation='softmax')(model1_layer1)

#define layer 1 for model 2
model2_layer1 = tf.keras.layers.Dense(8, activation='relu')(model2_inputs)

#define layer 2 for model 2
model2_layer2 = tf.keras.layers.Dense(4, activation='softmax')(model2_layer1)

#merge model 1 and model 2
merged = tf.keras.layers.add([model1_layer2, model2_layer2])

#define a functional model
model = tf.keras.Model(inputs=[model1_inputs, model2_inputs], outputs=merged)

#compile the model
model.compile('adam', loss='categorical_crossentropy')

*Training and Validation with keras

import tensorflow as tf

model = tf.keras.Sequential()

#define the hidden layer
model.add(tf.keras.layers.Dense(16, activation='relu', input_shape=(784,)))

#define the output layer
model.add(tf.keras.layers.Dense(4, activation='softmax'))

#compile the model
model.compile('adam', loss='categorical_crossentropy')

#train model
model.fit(image_features, image_labels)


-> Changing the metric

#Recompile the model with the accuracy metric
model.compile('adam', loss='categorical_crossentropy', metrics=['accuracy'])

#Train model with validation split
model.fit(features, labels, epochs=10, validation_split=0.20)


*Training models with the Estimators API

- High-level Tensorflow APIs: Estimators
- Mid-level Tensorflow APIs: layers, datsets, metrics
- Low-level Tensorflow APIs: Python

-> Estimators API are less fexible as it enforces best practices by placing restrictions on model architecture and training.
-> It allows for faster deployment. Also, many premade models.

-> Model specifcation and training:
   1. Define feature columns
   2. Load and transform data
   3. Define an estimator
   4. Apply train operation

1. Defining feature columns

import tensorflow as tf

#define a numeric feature column
size = tf.feature_column.numeric_column("size")

#define a categorical feature column
rooms = tf.feature_column.categorical_column_with_vocabulary_list("rooms", ["1","2","3","4","5"])

features_list = [size, rooms]

features_list = [tf.feature_column.numeric_column('image', shape=(784,))]


2. Loading and transforming data

#define input data function
def input_fn():
    #define feature dictionary
    features = {"size":[1340, 1690, 2720],"rooms":[1, 3, 5]}
    #define labels
    labels = [293838, 744004, 829003]
    return features, labels
    
    
3./4. Define and train a regression estimator

#define a deep neural network regression
model0 = tf.estimator.DNNRegressor(feature_columns = feature_list, hidden_units = [10, 6, 6, 3])

#train the regression model
model0.train(input_fn, steps=20)

-> Define and train a deep neural network

#define a deep neural network classifier
model1 = tf.estimator.DNNClassifier(feature_columns = feature_list, hidden_units = [32, 16, 8], n_classes=4)

#train the classifier
model1.train(input_fn, steps=20)



***INRODUCTION TO PYTORCH

-> PyTorch is an open source machine learning library used for developing and training neural network based deep learning models.

import torch
torch.tensor([[2,3,5], [1,2,9]])

torch.rand(2,2) (random matrix of 2x2)

a = torch.rand((3,5))
a.shape

*Matrix multiplication
a = torch.rand((2,2))
b = torch.rand((2,2))

torch.matmul(a,b)

*Zeros
a_torch = torch.zeros(2,2)

Ans: tensor([[0., 0.],[0., 0.]])

*Ones
b_torch = torch.ones(2,2)

Ans: tensor([[1., 1.],[1., 1.]])

*Eye
c_torch = torch.eye(2)

Ans: tensor([[1., 0.],[0., 1.]])

*Forward Propogation
-> Pytorch implementation

import torch

a = torch.Tensor([2])
b = torch.Tensor([-4])
c = torch.Tensor([-2])
d = torch.Tensor([2])

e = a + b
f = c * d

g = e * f
print(e, f, g)

*Backpropogation in PyTorch

import torch

x = torch.tensor(-3., requires_grad = True)
y = torch.tensor(5., requires_grad = True)
z = torch.tensor(-2., requires_grad = True)

q = x + y
f = q * z

f.backward()

print("Gradient of z is: " + str(z.grad))
print("Gradient of y is: " + str(z.grad))
print("Gradient of x is: " + str(z.grad))


*Fully connected neural networks

import torch

input_layer = torch.rand(10)

w1 = torch.rand(10, 20)
w2 = torch.rand(20, 20)
w3 = torch.rand(20, 4)
h1 = torch.matmul(input_layer, w1)
h2 = torch.matmul(h1, w2)
output_layer = torch.matmul(h2, w3)
print(output_layer)




**ACTIVATION FUNCTIONS

*Matrix multiplication is a linear transformation
input_layer = torch.tensor([2., 1.])
weight_1 = torch.tensor([[0.45, 0.32], [-0.12, 0.29]])
weight_2 = torch.tensor([[0.45, 0.34], [-0.19, 0.77]])
weight = torch.matmul(weight_1, weight_2)
output_layer = torch.matmul(input_layer, weight)
print(output_layer)
print(weight)

*RelU activation functions

import torch.nn as nn
relu = nn.ReLU()

tensor_1 = torch.tensor([2., -4.])
print(relu(tensor_1))

tensor_2 = torch.tensor([[2., -4.],[1.2, 0.]])
print(relu(tensor_2))

*CROSS ENTROPY LOSS IN PYTORCH

logits = torch.tensor([[3.2, 5.1, -1.7]])
ground_truth = torch.tensor([0])
criterion = nn.CrossEntropyLoss()

loss = criterion(logits, ground_truth)
print(loss)


*Preparing dataset in Pytorch

# Transform the data to torch tensors and normalize it 
transform = transforms.Compose([transforms.ToTensor(),transforms.Normalize((0.1307), ((0.3081)))])

# Prepare the datasets
trainset = torchvision.datasets.MNIST('mnist', train=True, download=True, transform=transform)
testset = torchvision.datasets.MNIST('mnist', train=False, download=True, transform=transform)

# Prepare the dataloaders
trainloader = torch.utils.data.DataLoader(trainset, batch_size=32, shuffle=True, num_workers=0)
testloader = torch.utils.data.DataLoader(testset, batch_size=32, shuffle=False, num_workers=0)  

# Compute the shape of the training set and testing set
trainset_shape = trainloader.dataset.train_data.shape
testset_shape = testloader.dataset.test_data.shape

# Print the computed shapes
print(trainset_shape, testset_shape)

# Compute the size of the minibatch for training set and testing set
trainset_batchsize = trainloader.batch_size
testset_batchsize = testloader.batch_size

# Print sizes of the minibatch
print(trainset_batchsize, testset_batchsize)


   
*Building a neural network

# Define the class Net
class Net(nn.Module):
    def __init__(self):    
    	# Define all the parameters of the net
        super(Net, self).__init__()
        self.fc1 = nn.Linear(28 * 28 * 1, 200)
        self.fc2 = nn.Linear(200, 10)

   def forward(self, x):    
    	# Do the forward pass
        x = F.relu(self.fc1(x))
        x = self.fc2(x)
        return x
        
# Instantiate the network, the Adam optimizer and Cross-Entropy loss function
model = Net()   
optimizer = optim.Adam(model.parameters(), lr=3e-4)
criterion = nn.CrossEntropyLoss()

for batch_idx, data_target in enumerate(train_loader):
    data = data_target[0]
    target = data_target[1]
    data = data.view(-1, 28 * 28)
    optimizer.zero_grad()

   # Complete a forward pass
   output = model(data)

   # Compute the loss, gradients and change the weights
   loss = criterion(output, target)
   loss.backward()
   optimizer.step()
