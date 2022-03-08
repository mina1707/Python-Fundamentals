# Python Syntax 
- Either use tab or space but NOT USE BOTH!
    1. Code Block: is a line of code following with the stuff that we want to execute. Ex:
        a. def --> functions
        b. if, elif, else --> conditional statements 
        c. for, while --> loops
        d. class --> classes

    Ex HOW TO INDENT 
        x = 10
    if x > 50:
    	print("bigger than 50")
    else:
    	print("smaller than 50")

- When we are not sure of our statement for declaring or even a variable we use "pass". EX:
    for val in my_string:
    pass

# Primitive Data Types 

    1. Boolean 
    2. Numberes
    3. Strings 

    ```Python

# Composite Data Types 

    # 1. Truples: This is a data type that is immutables and cannot be change. Ex: 
        dog = ('Bruce', 'cocker spaniel', 19, False)
        print(dog[0]) ----->		# output: Bruce
        dog[1] = 'dachshund'----->	# ERROR: cannot be modified ('tuple' object does not support item assignment)

    # 2. Lists: This is a type of data that is mutable and can hold a group of values. Ex:

        empty_list = []
        ninjas = ['Rozen', 'KB', 'Oliver']
        print(ninjas[2]) 	# output: Oliver
        ninjas[0] = 'Francis' ----> Notice that here we are replacing a value 
        ninjas.append('Michael')
        print(ninjas)	# output: ['Francis', 'KB', 'Oliver', 'Michael']
        ninjas.pop() -----> Notice that here we are poping the last value 
        print(ninjas)	# output: ['Francis', 'KB', 'Oliver']
        ninjas.pop(1) ----> and here we are poping value index 1.
        print(ninjas)	# output: ['Francis', 'Oliver']

    # 3. Dictionaries: a group of keys! Be awaye that dictionaries need a key to access the object.

        empty_dict = {}
        new_person = {'name': 'John', 'age': 38, 'weight': 160.2, 'has_glasses': False}
        new_person['name'] = 'Jack'	#----> updates if the key exists, adds a key-value pair if it doesn't
        new_person['hobbies'] = ['climbing', 'coding'] #----> ads a new value 
        print(new_person)	
        # output: {'name': 'Jack', 'age': 38, 'weight': 160.2, 'has_glasses': False, 'hobbies': ['climbing', 'coding']}
        w = new_person.pop('weight') #----> removes the specified key and returns the value
        print(w)		#----> output: 160.2
        print(new_person)	
        # output: {'name': 'Jack', 'age': 38, 'has_glasses': False, 'hobbies': ['climbing', 'coding']}       

    # 4. Common Functions: If we are unsure of a data's type we can use "type" 

        print(type(2.63))		# output: <class 'float'>
        print(type(new_person))		# output: <class 'dict'>

    #And. for length attributte, we can use "len"

        print(len(new_person))		# output: 4 (the number of key-value pairs)
        print(len('Coding Dojo'))	# output: 11
        we can remuve with del or .clear() and pop()

```
# NUMBERS
- There are 3 types of numbers in python 
    1- Int: this could be a whoe number, positive or negative.
    2- Float: Decimal number, positive or negative.
    3- Complex:

- How can we recognize the type of numbers? We can use: print(type(24))
- If we want to convert a number, we can use:
```python
    int_to_float = float(35)
    float_to_int = int(44.2)
    int_to_complex = complex(35)
    print(int_to_float)
    print(float_to_int)
    print(int_to_complex)
    print(type(int_to_float))
    print(type(float_to_int))
    print(type(int_to_complex))
```
- To get a RANDOM number:
```python
    import random
print(random.randint(2,5)) # provides a random number between 2 and 5, but not including 5!
```
# STRINGS 

```python 
ex: 
    name = "Zen"
    print("My name is", name) #---> output: Mi name is Zen

    name = "Zen"
    print("My name is " + name) #--->output: My name is Zen

#PYTHON DOES NOT KNOW HOW TO ADD A STRING AND A NUMBER!!!! SOOOOOOO WE DO THIS!!!!!!!!!

    print("Hello" + 42)			# output: TypeError
    print("Hello" + str(42))		# output: Hello 42 ---> Notice that we add str
When we use print we use str. And, when we want to reasign a value we use int

    total = 35
    user_val = "26"
    total = total + user_val		# output: TypeError
    total = total + int(user_val)		# total will be 61 ---> Notice that we want to use the string as a number!!
```

    ### F-strings (literal string interpolation)!!!!!!-Notice that we add an "f" 
        
```python 
    first_name = "Zen"
    last_name = "Coder"
    age = 27
    print(f"My name is {first_name} {last_name} and I am {age} years old.") #-->output: My name is Zen Coder and I am 27 years old.
```
    ### String-format - Notice that there should be the same numbers of {} and argunments to pass.

    ```python
    first_name = "Zen"
    last_name = "Coder"
    age = 27
    print("My name is {} {} and I am {} years old.".format(first_name, last_name, age))
    # output: My name is Zen Coder and I am 27 years old.
    print("My name is {} {} and I am {} years old.".format(age, first_name, last_name))
    # output: My name is 27 Zen and I am Coder years old.
```
    ### More examples to BUILT-IN string methods. BUT!! there are more, these is just the basic.

        string.upper(): returns a copy of the string with all the characters in uppercase.
        string.lower(): returns a copy of the string with all the characters in lowercase.
        string.count(substring): returns number of occurrences of substring in string.
        string.split(char): returns a list of values where string is split at the given character. Without a parameter the default split is at every space.

# Lists 
- Here is an example of lists: 
```python
    fruits = ['apple', 'banana', 'orange', 'strawberry']
    vegetables = ['lettuce', 'cucumber', 'carrots']
    fruits_and_vegetables = fruits + vegetables
    print(fruits_and_vegetables) #--> output:['apple','banana','orange','strawberry,'lettuce','cucumber','carrots']
    salad = 3 * vegetables 
    print(salad) #-->#-->putput: ['lettuce','cucumber','carrots,'lettuce','cucumber','carrots,'lettuce','cucumber','carrots,]
```

- It is important to know how to access the values in lists. EX: 
    drawer = ['documents', 'envelopes', 'pens']
    #access the drawer with index of 0 and print value
    print(drawer[0])  #prints documents
    #access the drawer with index of 1 and print value
    print(drawer[1]) #prints envelopes
    #access the drawer with index of 2 and print value
    print(drawer[2]) #prints pens

    ######## Manipulating lists: 

    EX-1

        x = [1,2,3,4,5]
        x.append(99)
        print(x) ---> the output would be [1,2,3,4,5,99]

    EX-2 
        x = [99,4,2,5,-3]
        print(x[:])
        #the output would be [99,4,2,5,-3]
        print(x[1:])
        #the output would be [4,2,5,-3];
        print(x[:4])
        #the output would be [99,4,2,5]
        print(x[2:4])
        #the output would be [2,5];

    EX-3 LEN

        my_list = [1, 'Zen', 'hi']
        print(len(my_list)) -------> output: 3, this checks the length of your list!
        

# DICTIONARIES 
- Remember that we need a key value to access dictionaries. 

    EX-1 

        weekend = {"Sun": "Sunday", "Sat": "Saturday"} ---> Sun is the key and Sunday is the value!
        capitals = {} --->create an empty dictionary then add values
        capitals["svk"] = "Bratislava" ---> this is how we add values
        capitals["deu"] = "Berlin"
        capitals["dnk"] = "Copenhagen"

    And, How do I ACCESS the value ?

    EX-2 

        print(weekend["Sun"]) ---> Rememeber that to acccess the value, the key needs quotation.
        print(capitals["svk"])

    Removing values 

    EX-3
        value_removed = capitals.pop('svk') # will remove the key 'svk' and return it's value
        del capitals['dnk'] # will delete the key, and not return anything


# CONDITIONALS 

    EX-1 
            x = 12
            if x > 50:
                print("bigger than 50")
            else:
                print("smaller than 50") ---> This is the only statemment that will execute. 
            

            x = 55
            if x > 10:
                print("bigger than 10") --->The first statement will execute, eventho x is bigger than 55!
            elif x > 50:
                print("bigger than 50")
            else:
                print("smaller than 10")
            

            if x < 10:
                print("smaller than 10") ---> nothing happens because the statement is false.
            


# LOOPS 

    EX-1 
        for x in range(0, 10, 2):
             print(x) ---> OUTPUT:0,2,3,6,8
        
        for x in range(5, 1, -3):
            print(x) ----> output: 5,2 

    EX-2 
        for x in 'Hello':
            print(x) ---> 'H', 'e', 'l', 'l', 'o'

    ### Loops through lists 

        my_list = ["abc", 123, "xyz"]
        for i in range(0, len(my_list)):
            print(i, my_list[i])
        ----> output: 0 abc, 1 123, 2 xyz
            
        # OR 
            
        for v in my_list:
            print(v)
        ----> output: abc, 123, xyz


    ### Loops through Dictionaries 

    EX-1

        my_dict = { "name": "Noelle", "language": "Python" }
            for k in my_dict:
                print(k) ---> output: name, language
    
    EX-2 

        my_dict = { "name": "Noelle", "language": "Python" }
            for k in my_dict:
                print(my_dict[k]) ---> output: Noelle, Python
    EX-3 

        capitals = {"Washington":"Olympia","California":"Sacramento","Idaho":"Boise","Illinois":"Springfield","Texas":"Austin","Oklahoma":"Oklahoma City","Virginia":"Richmond"}
            # another way to iterate through the keys
            for key in capitals.keys():
                print(key)
            ---->output: Washington, California, Idaho, Illinois, Texas, Oklahoma, Virginia
            #to iterate through the values
            for val in capitals.values():
                print(val)
            ----> output: Olympia, Sacramento, Boise, Springfield, Austin, Oklahoma City, Richmond
            #to iterate through both keys and values
            for key, val in capitals.items():
                print(key, " = ", val)
            ----> output: Washington = Olympia, California = Sacramento, Idaho = Boise, etc

# BREAK 

    


        

                    




        























 






