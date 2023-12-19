# encrypt-decrypt-in-python
this program is for encryption and decryption of a sentence
import string
import random
# String = ''.join(random.choices(string.ascii_letters))
a = input("Enter C for coding and D for decoding: ")
list3 = []

if a == "C":
    x = input("Enter your sentence: ")
    list1 = list(x.split())

    for i in list1:
        list2 = list(i)
        if len(list2) <= 3:
            list2.reverse()
            list3.extend(list2)
            
        else:
            list2.append(list2[0])
            list2.remove(list2[0])
            list2.insert(0, ''.join(random.choices(string.ascii_letters)))
            list2.insert(0, ''.join(random.choices(string.ascii_letters)))
            list2.insert(0, ''.join(random.choices(string.ascii_letters)))
            list2.append(''.join(random.choices(string.ascii_letters)))
            list2.append(''.join(random.choices(string.ascii_letters)))
            list2.append(''.join(random.choices(string.ascii_letters)))
            list3.extend(list2)
    print(list3)


elif(a=="D"):
    y = input("Enter the coded sentence with space for each string of the sentence:")
    list4 = list(y.split())
    for j in list4:
        list5 = list(j)
        if(len(list5)<=3):
            list5.reverse()
            list3.extend(list5)
        else:
            list5.pop(len(list5)-1)
            list5.pop(len(list5)-1)
            list5.pop(len(list5)-1)
            list5.pop(0)
            list5.pop(0)
            list5.pop(0)
            
            list5.insert(0,list5[len(list5)-1])
            list5.pop(len(list5)-1)
            list3.extend(list5)
    print(list3)   
