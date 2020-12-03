A# Title
**Dev:** *AButt*  
**Date:** *12.3.20*
## Introduction
###This provides a brief description of what's going on in this assigment. The assigmnent was to learn about Pickling and Exception handling. 
## The Code
```
# ------------------------------------------------- #
# Title: Assignment 07-4Credit
# Description: Storing data in a binary file
# ChangeLog: (Ahson Butt, 12-01-20, Created Script)
# ------------------------------------------------- #

#saving cats to a pickled file
#collect user inputs

#import the pickle module
import pickle
''' collect user inputs and create variables'''

cat_name = input("Please enter your cat's name:") #had this
age = int(input("Please enter it's age:")) #Had this
cat_list = [cat_name, age] #thought I had line 14, actual code
#commented out under 'create variables'
print(cat_list) #added this

'''create variables'''
#cats = []
#all_cats = cat_name, age
#cats.append(all_cats)

''' Open and append the file that cat names are being saved to'''
objFile = open("all_cats.dat", "ab") #used 'file' insted of objFile.. this is not a variable
#no matter how hard I try to make it one.
pickle.dump(cat_list, objFile)#replaced all_cats and file
objFile.close() #replaced file

''' Open and append the file that cat names are being saved to'''
objFile = open("all_cats.dat", "rb") #replace file
objFileData = pickle.load(objFile) #replaced cats and file, objFileData is not a variable

objFile.close() #replaced file
print(objFileData) #replaced cats

print("Lets try to open another file!")
try:
    f = open("all_cats.datZ", "rb")
except:
    print("there was an error! <<Copied Custom Code")

'''I was trying to write an exception to where if I put in my dog's
name, I would have gotten the error message "Andi is a dog, she 
doesn't go into the Cats list" I couldn't figure out how to get it to 
work in the data gathering section. Whether a cat name or Andi was put in,
I was still getting the exception regardless. I dumped the code out of 
frustration... in hindsight I should have kept it. '''
```
### Image Section

## Summary
Thanks!
