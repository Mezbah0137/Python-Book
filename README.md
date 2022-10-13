# Python-Book
These are some regular problem solving through python.
Task 1

Assume, you have been given a tuple.

a_tuple = ("The Institute", ("Best Mystery & Thriller", "The Silent Patient", 68821), 75717, [1, 2, 3, 400, 5, 6, 7], ("Best Fiction", "The Testaments", 98291))

Write one line of Python code to access and print the value 400.

[ ]
a_tuple = ("The Institute", ("Best Mystery & Thriller", "The Silent Patient", 68821), 75717, [1, 2, 3, 400, 5, 6, 7], ("Best Fiction", "The Testaments", 98291))

print(a_tuple[3][3])
400
Task 2

Assume, you have been given a tuple. Write a Python program that creates a new tuple excluding the first and last two elements of the given tuple and prints the new tuple.

Hint: You may use tuple slicing.
[ ]
a_tuple = (10, 20, 24, 25, 26, 35, 70)
length = len(a_tuple)

if length > 3:
  print(a_tuple[2:length-2])
(24, 25, 26)
Task 3

Assume, you have been given a tuple.

book_info = ( ("Best Mystery & Thriller","The Silent Patient",68,821), ("Best Horror","The Institute",75,717), ("Best History & Biography","The five",31,783 ), ("Best Fiction","The Testaments",98,291) )

Write a Python program that prints the size of the tuple and all its elements as shown below.

Output:
Size of the tuple is: 4

('Best Mystery & Thriller', 'The Silent Patient', 68, 821)

('Best Horror', 'The Institute', 75, 717)

('Best History & Biography', 'The five', 31, 783)

('Best Fiction', 'The Testaments', 98, 291)

[ ]
book_info = ( ("Best Mystery & Thriller","The Silent Patient",68,821), ("Best Horror","The Institute",75,717), ("Best History & Biography","The five",31,783 ), ("Best Fiction","The Testaments",98,291) )
length = len(book_info)

print("Size of the tuple is: ",length)

for i in book_info:
  print(i)
Size of the tuple is:  4
('Best Mystery & Thriller', 'The Silent Patient', 68, 821)
('Best Horror', 'The Institute', 75, 717)
('Best History & Biography', 'The five', 31, 783)
('Best Fiction', 'The Testaments', 98, 291)
Task 4

Assume, you have been given a tuple with details about books that won the Good Reads Choice Awards.

book_info = ( ("Best Mystery & Thriller","The Silent Patient",68821), ("Best Horror","The Institute",75717), ("Best History & Biography","The five",31783 ), ("Best Fiction","The Testaments",98291) )

Write a Python program that prints the award category, the book name, and its total votes earned as shown below.

[Must use Tuple unpacking for printing and need to handle the quotation marks as a partof the output]
Output:

The Silent Patient won the 'Best Mystery & Thriller' category with 68821 votes

The Institute won the 'Best Horror' category with 75717 votes

The five won the 'Best History & Biography' category with 31783 votes

The Testaments won the 'Best Fiction' category with 98291 votes

[ ]
book_info = ( ("Best Mystery & Thriller","The Silent Patient",68821), ("Best Horror","The Institute",75717), ("Best History & Biography","The five",31783 ), ("Best Fiction","The Testaments",98291) )

category = [lis[0] for lis in book_info]
name = [lis[1] for lis in book_info]
vote = [lis[2] for lis in book_info]

length = len(category)

for i in range(length-1):
  print(name[i]+' won the '+category[i]+' category with '+str(vote[i])+' votes')

The Silent Patient won the Best Mystery & Thriller category with 68821 votes
The Institute won the Best Horror category with 75717 votes
The five won the Best History & Biography category with 31783 votes
Task 5

Write a python program that takes an input from the user and finds the number of times that the input is present in a given tuple.

[ ]
 a_tuple = (10, 8, 5, 2, 10, 15, 10, 8, 5, 8, 8, 2)
 number = int(input('Sir, please enter your desired number: '))
 counter = 0
 for i in a_tuple:
   if i == number:
     counter = counter+1
 
 print("{} appears {} times in tuple".format(number,counter))

Sir, please enter your desired number: 8
8 appears 4 times in tuple
Task 6

Write a Python program to reverse a given tuple.

[You are not allowed to use tuple slicing]

Note: Unlike lists, tuples are immutable. So, in order to reverse a tuple, we may need to convert it into a list first, then modify the list, and finally convert it back to a tuple.
[ ]
a_tuple = ('a', 'b', 'c', 'd', 'e', 'f', 'g', 'h')
a_list = list(a_tuple)

print(tuple(a_list[-1: :-1]))

('h', 'g', 'f', 'e', 'd', 'c', 'b', 'a')
Task 7

Suppose you are given two dictionaries. Now create a new dictionary "marks", merging the two dictionaries, so that the original two dictionaries remain unchanged.

Note: You can use dictionary functions.
Given:
{'Harry':15, 'Draco':8, 'Nevil':19}

{'Ginie':18, 'Luna': 14}

Output:
{'Harry': 15, 'Draco': 8, 'Nevil': 19, 'Ginie': 18, 'Luna': 14}

Given:
{'A':90, 'B': 0}

{'C':50}

Output:
{'A': 90, 'B': 0, 'C': 50}

[ ]
dict1 = {'Harry':15, 'Draco':8, 'Nevil':19}
dict2 = {'Ginie':18, 'Luna': 14}
mark = {}

for i in dict1:
  mark[i] = dict1[i]

for j in dict2:
  mark[j] = dict2[j]

print(mark)

{'Harry': 15, 'Draco': 8, 'Nevil': 19, 'Ginie': 18, 'Luna': 14}
[ ]
def Merge(dict1, dict2):
    return(dict1.update(dict2))

dict1 = {'a': 90, 'b': 0}
dict2 = {'d': 50}

print(Merge(dict1, dict2))
print(dict1)
None
{'a': 90, 'b': 0, 'd': 50}
Task 8

Write a Python program that takes a dictionary as an input from the user and then prints the average of all the values in the dictionary.

[You are not allowed to use len() and sum()]
Hint (1): For taking dictionary input

Approach (1): For taking dictionary as an input from the user, you may take the whole dictionary as a string using the input() function. Then you can use the split(), strip() functions and conditions to get the keys and values from the string. Finally, you can make the dictionary using the obtained data.

Approach (2): If the first approach seems too difficult you can create an empty dictionary and then just run a simple loop. For each iteration ask the user for a key and a value using the input() function and keep updating the dictionary with the key and value.

Hint (2): After you have a dictionary, you can use dictionary functions to get all the values from it, run loop to calculate the sum and the total number of values in the dictionary in order to find out the average.

[ ]

dict1 = {}
element = int(input('Sir, please enter number of elements: '))

for i in range(element):
  name = input('Sir, please enter your desired name: ')
  number = int(input('Sir, please enter your desired number: '))

  dict1[name] = number

print(dict1)

length = len(dict1)
sum = 0

for j in dict1:
  sum = sum + dict1[j]

average = sum/length

print("Average is: ",average)






Sir, please enter nuber of elements: 3
Sir, please enter your desired name: Kishore
Sir, please enter your desired number: 250
Sir, please enter your desired name: Musa
Sir, please enter your desired number: 110
Sir, please enter your desired name: Robin
Sir, please enter your desired number: 230
{'Kishore': 250, 'Musa': 110, 'Robin': 230}
Average is:  196.66666666666666
Task 9

Suppose there is a dictionary named exam_marks as given below.

exam_marks = {'Cierra Vega': 175, 'Alden Cantrell': 200, 'Kierra Gentry': 165, 'Pierre Cox': 190}

Write a Python program that takes an input from the user and creates a new dictionary with only those elements from 'exam_marks' whose keys have values higher than the user input (inclusive).

[ ]
exam_marks = {'Cierra Vega': 175, 'Alden Cantrell': 200, 'Kierra Gentry': 165, 'Pierre Cox': 190}
n_dict = {}
user = int(input('Sir, please enter your desired number: '))

for i in exam_marks:
  if exam_marks[i] > user:
    n_dict[i] = exam_marks[i]

print(n_dict)
Sir, please enter your desired number: 170
{'Cierra Vega': 175, 'Alden Cantrell': 200, 'Pierre Cox': 190}
Task 10

Write a Python program that finds the largest value with its key from a given dictionary.

[You are not allowed to use the max() function for this task]
Note: You do not need to take the dictionaries as an input from the user but your code should work for any given dictionary. Also, you need to handle the quotation marks as a part of the output.

Hint: Think of membership operators (in and not in). You can use dictionary functions to get the values.

[ ]
g_dict = {'sci fi': 12, 'mystery': 15, 'horror': 8, 'mythology': 10, 'young_adult': 4, 'adventure':14}
max = 0

for i in g_dict:
  if g_dict[i] > max:
    max = g_dict[i]

print('The highest selling book genre is {} and the number of books sold are {}.'.format(i, max))

The highest selling book genre is adventure and the number of books sold are 15.
Task 11

Write a Python program that takes a String as an input from the user and counts the frequency of each character using a dictionary. For solving this problem, you may use each character as a key and its frequency as values.

[You are not allowed to use the count() function]
Hint: You can create a new dictionary to store the frequencies. You may ignore case for simplicity (i.e. may consider P and p to be the same).

[ ]
string = input('Enter your desired string: ')
dict1 = {}

for char in string:
  if char.isalpha():
    char = char.lower()
    
    if char in dict1:
      dict1[char] += 1
    else:
      dict1[char] = 1

print(dict1)

Enter your desired string: I love Python Programming
{'i': 2, 'l': 1, 'o': 3, 'v': 1, 'e': 1, 'p': 2, 'y': 1, 't': 1, 'h': 1, 'n': 2, 'r': 2, 'g': 2, 'a': 1, 'm': 2}
Task 12

Suppose you are given the following dictionary where the values are lists.

dict_1 = {'A': [1, 2, 3], 'b': ['1', '2'], "c": [4, 5, 6, 7]}

Write a Python program that counts the total number of items in a dictionary’s values and prints it.

[Without using sum(), len(), count() functions]

Note: Make changes to the above dictionary and see if your code works properly for other dictionaries as well.
[ ]
dict_1 = {'A': [1, 2, 3], 'b': ['1', '2'], "c": [4, 5, 6, 7]}
count = 0

for i,j in dict_1.items():
  for k in j:
    count += 1
    
print(count)
9
Task 13

Suppose you have been given the following list of tuples.

list_1 = [("a", 1), ("b", 2), ("a", 3), ("b", 1), ("a", 2), ("c", 1)]

Write a Python program that converts this list of tuples into a dictionary and then prints the dictionary.

[You are not allowed to use set]

Hint: Think of membership operators (in and not in).
[ ]
list_1 = [("a", 1), ("b", 2), ("a", 3), ("b", 1), ("a", 2), ("c", 1)]
dict_1 = {}

for i in list_1:
  dict_1[i[0]] = 0

for i in dict_1:
  list_2 = []

  for j in list_1:
    if i == j[0]:
      list_2 += [j[1]]

  dict_1[i] = list_2

print(d)
{'a': [1, 3, 2], 'b': [2, 1], 'c': [1]}
Tracing

[ ]
dict1 = {'a':59 , 'b':-82 , 'c':5 , 'd':-81 , 'e':53}
for i in dict1:
  j = 0
  k = 22
  while j < 5:
    if j % 2 == 0:
      k = dict1[i] + j - (8 + k % 6) / 3
      dict1[i] = dict1[i]+ int(k)
    else:
      k = dict1[i] + j - (6 - k % 8) * 3
      dict1[i] = dict1[i] - int(k)
    j += 1
  print(int(k))
  print(i + " -> " + str(dict1[i]))
8
a -> 17
10
b -> 19
2
c -> 5
-7
d -> -14
2
e -> 5
