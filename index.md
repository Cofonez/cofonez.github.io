## Below is a couple examples of python projects that i've been working on in my spare time





### 

```markdown
Python Code Projects

#establishing some variables that we will increment
#for whenever we find an integer that fits the criteria
less = 0
greater = 0
equal = 0
counter = 0

import random 

#code = [random.randint(0,9),random.randint(0,9),random.randint(0,9),random.randint(0,9)]

code=""
for r in range(4):
    x=random.randint(1,9)
    x =str(x)
    code = code+x


guess = input("enter your 4 digit guess: ")

if '0' in guess:
    print(code)

#error handling for entries less than or greater than 4
if len(guess) != 4:
    guess =input("The code is 4 numbers long, please only enter 4 digits: ")
    

#error handling for non numeric input
if guess.isdigit() == False:
    guess = input("Please only enter digits: ")

done = False
while not done:
    while equal != 4:
        while counter < len(code):
            if code[counter]==guess[counter]:
                equal+=1
            elif code[counter] > guess[counter]:
                greater+=1
            else:
                less += 1
            counter += 1
            if equal == 4:
                print("congratulations you guessed the code correctly")
                done = True
            
        if equal != 4:
            print("Your clue is" + "=" * equal + "<" * less + ">" *greater)
            less=0
            greater=0
            counter=0
            equal=0
            guess = input("enter your 4 digit guess: ")
            if '0' in guess:
                print(code)



# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Cofonez/cofonez.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
