# PA 1
## Problem 1 : Create a function that takes a string and returns a string with its letters in alphabetical order.

```py
def sortfunction(string):                          #function declaration
```
### Step 1: We define a function by giving it a name and a variable which we will define later. In this case we used the name "sortfunction" to name our function and "(string)" as its variable

```py
print('-'.join(sorted(string)))                #joining the sorted string with "-" in between them
```

### Step 2: We sort the string using the call "sorted(string)" and we join it all together using the ".join", while having the string "-" in between the joined, sorted, strings. Simultaneously, while calling so, we can print it so we can use the function here on out

```py
sortfunction("quickbrownfoxjumpsoverthelazydog")
OUTPUT: a-b-c-d-e-e-f-g-h-i-j-k-l-m-n-o-o-o-o-p-q-r-r-s-t-u-u-v-w-x-y-z
```

### Step 3: Lastly, we call the function with the associated string assigned in the variable of the original function, which is string


---------------------------------------------------------------------------------------------------------------------

## Problem 2: Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon

```py
strings = [                                           #Inputted string data to be compared to the keys in the dictionary below
    "Look at my smile",
    "You make me Grin",
    "Now I am Sad",
    "YOU MAKE ME SO MAD",
    "I can't smile"
```

### Step 1: First we can input the list of strings that we would use and convert later on. These strings would have the words that we would associate with the keys in the dictionaries later on.

```py
emoticons = {                                        #Dictionary sorted as word:emoji respectively
    "smile": ":)",
    "grin": ":D",
    "sad": ":((",
    "mad": ">:("
```

### Step 2: We utilize a dictionary to contain the words that we have to look for in the given strings, and the values that we associate them with. The keys and values of this specific dictionary is declared in the code as; word and emoji, respectively.

```py
for s in strings:                                    #for loop that goes through each element in the list strings
```

### Step 3: We use a for loop to go through each element of the list "strings"

```py
for word, emoji in emoticons.items():            #for loop that goes through the items inside the dictionary
```

### Step 4: We use another for loop, but this time for the code to go through each keys and their associated values in the dictionary

```py
 if word in s:                                #checking for keys that are comparable to the strings
      s = s.replace(word, emoji)               #line that replaces the compared strings and keys into values called emoji
```

### Step 5: We check for the keys that are also present in the string and we replace the word that is equal to an individual key with its associated value

```py
if word.capitalize() in s:                   #checking for capitalization (capital first word "Angry")
    s = s.replace(word.capitalize(), emoji)  #replaces capitalized word
```

### Step 6: We check for strings that has their first word capitalized, comparing it to the lower-cased dictionary keys, and replacing similar strings for their respective value (emoticons)

```py
if word.upper() in s:                        #checking for strings that are in all-caps
    s = s.replace(word.upper(), emoji)       #replaces all-capped word
```

### Step 7: We check for strings that are in upper-cased, comparing it again to the lower-cased dictionary keys, and replacing similar strings for their respective value (emoticons)

```py
 print(s)                                         #we print the updated version of s
```

### Step 8: Finally, we print the latest version of the variable "s" that has been updated throughout the code

--------------------------------------------------------------------------------------------------------------------

## Problem 3: Unpack the list write your code here into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

```py
list = [1, 10, 2, 3, 4, 5, 6, 7, 8, 9]              #list declaration
```

### Step 1: First, we define the list and the elements within the list. In my example, I put what would be the last element on the second position so I can use extended unpacking for all the other elements.

```py
first, last, *middle = list                         #unpacking the list
```

### Step 2: We unpack the list. Note that we should consider the order of elements from left to right when unpacking a list

```py
print("First: ", first)                             #printing the list with string "First: " then unpacked element of the list using first
```

### Step 3: We use the syntax print to print the unpacked element of the list along with the string "First" in order to label it accordingly.

```py
print("Middle: ", *middle)                          #printing the list with string "Middle: " then the remaining unpacked elements assigned in *middle
```

### Step 4: Again, we use the syntax print to print the label for the middle unpacked elements. But note that the unpacked element that is contained in *middle are the ones that were unpacked using extended unpacking, meaning, it is all the other elements aside from the first and the last.

```py
print("Last: ", last)                               #printing the list with string "Last: " then unpacked element of the list using last
```

### Step 5: Finally, we print the final element that we have, which is the second element from left to right, along with its label so as to avoid confusion and remain cleanliness in the output.

# END
