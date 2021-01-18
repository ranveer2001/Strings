STRINGS

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
          



          
