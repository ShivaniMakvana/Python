# Python

- List Tuples Sets and Dictionary Data types in Python
[List_Tuple_Sets_Dict.ipynb](https://github.com/ShivaniMakvana/Python/blob/main/List_Tuple_Sets_Dict.ipynb)


## List

**In [1]:**```
subjects = ['History', 'Math', 'Physics', 'CS']```

**In [2]:**```
print(subjects) 
#Prints all the elements of the list```

['History', 'Math', 'Physics', 'CS']

**In [3]:**```
print(len(subjects))
#Prints number of elements in list```

4

**In [4]:**```
print(subjects[0])
#Prints the 1st element (History)```
History

**In [5]:**```
print(subjects[-1])
#Prints the last element (History)```
CS

**In [6]:**```
print(subjects[:2])
#Prints the 1st & 2nd element (History)
print(subjects[:2])```
['History', 'Math']
['History', 'Math']

**In [7]:**```
subjects.append('DS')
#Adds the item at the end of the list
print(subjects)```
['History', 'Math', 'Physics', 'CS', 'DS']

**In [8]:**```
subjects.insert(0,'DBMS')
#Adds the item at index 0
print(subjects)```
['DBMS', 'History', 'Math', 'Physics', 'CS', 'DS']

**In [9]:**```subjects_2 = ['Art', 'Design', 'Chemistry']```

**In [10]:**```
#subjects.insert(0,subjects_2)
#print(subjects)
#Let's try to add elements of subject_2 to subjects
#it got added as a seperate list in element 0, rather than splitting the items in subject_2 then adding them```

**In [11]:**```
subjects.extend(subjects_2)
print(subjects)
#Adds each element seperately to subject_2 at the end of the list```

['DBMS', 'History', 'Math', 'Physics', 'CS', 'DS', 'Art', 'Design', 'Chemistry']

**In [12]:**```
subjects.remove('Math')
#Finds & Removes Math from the list
print(subjects)```

['DBMS', 'History', 'Physics', 'CS', 'DS', 'Art', 'Design', 'Chemistry']

**In [13]:**```
popped = subjects.pop()
#Removes the last item in the list
print(subjects)
print(popped)
#Grabs the popped item```

['DBMS', 'History', 'Physics', 'CS', 'DS', 'Art', 'Design']
Chemistry

**In [14]:**```
subjects.reverse()
#Reverses the list
print(subjects)```

['Design', 'Art', 'DS', 'CS', 'Physics', 'History', 'DBMS']

**In [15]:**```
subjects.sort()
#Sorts the list in alphabetical order
print(subjects)
num_list = [2,6,4,5,3,1]
num_list.sort()
print(num_list)```

['Art', 'CS', 'DBMS', 'DS', 'Design', 'History', 'Physics']
[1, 2, 3, 4, 5, 6]

**In [16]:**```
print(min(num_list))
print(max(num_list))
print(sum(num_list))```

1
6
21

**In [17]:**```
print(subjects.index('CS'))
#Returns the index value of the item```

1

**In [18]:**```
print('Art' in subjects)
#Checks weather the item is present in the list or not```

True

**In [19]:**```
for item in subjects:
    print(item)
#Prints each item in new line```

Art
CS
DBMS
DS
Design
History
Physics

**In [20]:**```
for index,subject in enumerate(subjects):
    print(index,subject)
#Print the items along with index numbers starting from 0. this is done by enumerate() function```

0 Art
1 CS
2 DBMS
3 DS
4 Design
5 History
6 Physics

**In [21]:**```
for index,subject in enumerate(subjects,start=1):
    print(index, subject)
#Print the items along with index numbers starting from 1. this is done by enumerate() function```

1 Art
2 CS
3 DBMS
4 DS
5 Design
6 History
7 Physics

**In [22]:**```
subject_str = ' - '.join(subjects)
print(subject_str)
#turns list into '-' seperated string```

Art - CS - DBMS - DS - Design - History - Physics

**In [23]:**```
new_list = subject_str.split('-')
print(new_list)
#Creates the list, just reverse of .join()```

['Art ', ' CS ', ' DBMS ', ' DS ', ' Design ', ' History ', ' Physics']
