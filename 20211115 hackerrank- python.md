
    PreparePythonIntroductionPython If-Else

Python If-Else

```pycon
import math
import os
import random
import re
import sys
if __name__ == '__main__':
    n = int(input().strip())
    if n%2!=0 and n>=2 and n<=5:
        print('Weird')
    elif n%2==0 and n>=2 and n<=5:
        print('Not Weird')
    elif n%2==0 and n>=6 and n<=20:
        print('Weird')
    elif n>20:    
        print('Not Weird')
    else:
        print('error')


import math
import os
import random
import re
import sys
if __name__ == '__main__':
    n = int(input().strip())
    if n%2!=0 and n>=2 and n<=5:
        print('Weird')
    elif n%2==0 and n>=2 and n<=5:
        print('Not Weird')
    elif n%2==0 and n>=6 and n<=20:
        print('Weird')
    elif n>20:    
        print('Not Weird')
    else:
        print('')

import math
import os
import random
import re
import sys
if __name__ == '__main__':
    n = int(input().strip())
    if n%2!=0:
        print('Weird')
    elif n%2==0 and n>=2 and n<=5:
        print('Not Weird')
    elif n%2==0 and n>=6 and n<=20:
        print('Weird')
    elif n>20:    
        print('Not Weird')
    else:
        print('')
```
__________________

    PreparePythonIntroductionArithmetic Operators

Arithmetic Operators

```pycon
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    class Calculator:
        def __init__(self, n, m):
            self.n = n
            self.m = m
        def addition(self, n, m):
            add= n+m;
            return self.add
        def subtract(self, n, m):
            sub= n-m;
            return self.sub        
        def multiply(self, n, m):
            mul= n*m;
            return self.mul
    print(Calculator.addition(a, b));
    print(Calculator.subtract(a, b));
    print(Calculator.multiply(a, b));
```

Attempt at class based answer- failed. 

```pycon
import math
import os
import random
import re
import sys
class Calculator:
    def __init__(self, n, m):
        self.n = n
        self.m = m
    def addition(self, n, m):
        add= n+m;
        return self.add
    def subtract(self, n, m):
        sub= n-m;
        return self.sub        
    def multiply(self, n, m):
        mul= n*m;
        return self.mul
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    calc= Calculator(a,b);
    print(calc.addition(a, b));
    print(calc.subtract(a, b));
    print(calc.multiply(a, b));
```

My Answer-
```pycon
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a+b);
    print(a-b);
    print(a*b);
```

Discussion answers interesting-

```pycon
print(a+b,a-b,a*b, sep="\n")
    
tambah, tolak, darab = a+b, a-b, a*b
print(tambah)
print(tolak)
print(darab)


def fun(m,n):
    print(m+n,m-n,m*n,sep="\n")
    return
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    fun(a,b)

a = int(input())
b = int(input())
def operaciones (a,b):
    suma = a+b
    print (suma)
    resta = a-b
    print (resta)
    multiplicacion = a*b
    print (multiplicacion)
operaciones (a,b)


def function(a, b):
    print(a+b)
    print(a-b)
    print(a*b)
a = int(raw_input())
b = int(raw_input())
function(a, b)

if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a//b);
    print(a/b);
    /*
    if b== 0:
	print('error');
    else: 
	print(a/b);
        */
```        
________________

    PreparePythonIntroductionLoops

Loops

My answer-

```pycon
if __name__ == '__main__':
    n = int(input())
    list= []; #Define list.
    for a in range(0, n):
        list.append(a) 
        print(a*a);

if __name__ == '__main__':
    n = int(input())
    for a in range(0, n):
        print(a*a);
```

```pycon
def is_leap(year):
    leap = False
    # Write your logic here
    if year%4==0:
        leap= True;
        if year%100:
            leap= False;
            if year%400:
                leap= True;
    return leap
year = int(input())
```

My Answer- 

```pycon
def is_leap(year):
    leap = False
    # Write your logic here
    if year%4==0:
        leap= True;
        if year%100==0:
            leap= False;
            if year%400==0:
                leap= True;
    return leap
year = int(input())
```
____________________

    PreparePythonIntroductionPrint Function

Print Function

```pycon
from __future__ import print_function

if __name__ == '__main__':
    n = int(raw_input())
    for a in range(1, n+1):
        print(a , end ='' );
```
__________________

    PreparePythonRegex and ParsingGroup(), Groups() & Groupdict()

Group(), Groups() & Groupdict()
```pycon
import re
if __name__ == '__main__':
    S = input()
    #print (S);
    out= re.findall("+", S)
    print(out);
    #x = re.findall(".+", S)
```

Discussion answer- 
```pycon
import re
m = re.search(r'([a-zA-Z0-9])\1+', input().strip())    # Also could use (\w(?!_))\1+ as the regular expression. 
print(m.group(1) if m else -1)
```
_____________________


    PreparePythonRegex and ParsingRe.findall() & Re.finditer()

Re.findall() & Re.finditer()

```pycon
import re
m = re.search(r'([a-zA-Z0-9])\1+', input().strip())    # Also could use (\w(?!_))\1+ as the regular expression. 
print(m.group(1) if m else -1)
```

Discussion answers-
```pycon
import re
s = '[qwrtypsdfghjklzxcvbnm]'
a = re.findall('(?<=' + s +')([aeiou]{2,})' + s, input(), re.I)
print('\n'.join(a or ['-1']))
```

?    Causes the resulting RE to match 0 or 1 repetitions of the preceding RE. ab? will match either ‘a’ or ‘ab’.

(?<=...)    Matches if the current position in the string is preceded by a match for ... that ends at the current position. This is called a positive lookbehind assertion. (?<=abc)def will find a match in 'abcdef', since the lookbehind will back up 3 characters and check if the contained pattern matches. The contained pattern must only match strings of some fixed length, meaning that abc or a|b are allowed, but a* and a{3,4} are not. Note that patterns which start with positive lookbehind assertions will not match at the beginning of the string being searched; you will most likely want to use the search() function rather than the match() function:
``` pycon
    >>>import re
m = re.search('(?<=abc)def', 'abcdef')
m.group(0)
```
'def'
This example looks for a word following a hyphen:
``` pycon
>>>m = re.search(r'(?<=-)\w+', 'spam-egg')
m.group(0)
'egg'
```

+    Causes the resulting RE to match 1 or more repetitions of the preceding RE. ab+ will match ‘a’ followed by any non-zero number of ‘b’s; it will not match just ‘a’.

``` pycon
match = re.findall(r'(?<=['+consonants+'])(['+vowels+']{2,})(?=['+consonants+'])',raw_input(),flags = re.I)
```

(?=...)    Matches if ... matches next, but doesn’t consume any of the string. This is called a lookahead assertion. For example, Isaac (?=Asimov) will match 'Isaac ' only if it’s followed by 'Asimov'.

``` pycon
# Enter your code here. Read input from STDIN. Print output to STDOUT
import re
s = '[qwrtypsdfghjklzxcvbnm]'
a = re.findall('(?<=' + s +')([aeiou]{2,})' + s, input(), re.I)
print('\n'.join(a or ['-1']))
```

Interesting regex answer-

``` pycon
import re
e=re.findall(r'(?<=[^aieou])([aeiou]{2,})(?=[^aieou])', input().strip(), re.I)
print(*e if e!=[] else [-1], sep='\n')
```
______________________

    PreparePythonRegex and ParsingRe.start() & Re.end()

Re.start() & Re.end()

``` pycon
import re
S = input()
k = input()
m = re.search(r'(?<=k)',S)
m.end();
m.start();
print(m.end(), m.start());
```

Discussion answer-

``` pycon
import re
s = input()
k = input()
index = 0
if re.search(k, s):
    while index+len(k) < len(s):
        m = re.search(k, s[index:]) #begins search with new index
        print("({0}, {1})".format(index+m.start(), index+m.end()-1)) 
        index += m.start() + 1 #assign new index by +1 
else:
    print((-1, -1))
```

``` pycon
import re
s = input()
print (s);
k = input()
print (k);
if (input()):
    l = input()
    print (l);
else:
    print('No further inputs');
```

``` pycon
import re
s = input()
print (s);
k = input()
print (k);
m = re.search(r'(?<='+ k +')',s, );
print(m);
print(m.start());
print(m.end());
```
``` pycon
import re
text, pattern = input(), input()
m= list(re.finditer("(?=(%s))"%pattern,text))
if not m:
    print((-1,-1))
for i in m:
    print((i.start(1),i.end(1)-1))
```
________________


    PreparePythonRegex and ParsingRegex Substitution

Regex Substitution

``` pycon
re.sub(r"\d+", square, "1 2 3 4 5 6 7 8 9")
```

/s/&/&/s 	#I think &, | are escape characters so they need / before them. /s... /s means that spaces are either side of the search term.
/s/|/|/s

or could match ' && ' or ' || '.

``` pycon
import re
string= input();
#for input():
#    string= string+ input();
string= re.sub(r"/s&&/s", " and ", string);
print (string);
string= re.sub(r"/s/|/|/s", " or ", string);
print (string);
```

``` pycon
import re
print('\n'.join(re.sub(R'(?<= )(&&|\|\|)(?= )', lambda x: 'and' if x.group()=='&&' else 'or', input()) for _ in range(int(input().strip()))))
```

Discussion answer-

``` pycon
import re
S=int(input())
for i in range(S):
      pattern1=re.compile(r'(?<= )(&&)(?= )')
      pattern2=re.compile(r'(?<= )(\|\|)(?= )')
      print(pattern2.sub('or', pattern1.sub('and', input())))
```

Tried unsuccessfully-

``` pycon
import re
S=int(input());
T= S;
for i in range(T):
        T= re.sub(r'(?<= )(&&)(?= )', 'and', T);
        #T=re.sub(r'(?<= )(&&)(?= )')
        T= re.sub(r'(?<= )(\|\|)(?= )', 'or', T);
        #T=re.sub(r'(?<= )(\|\|)(?= )')
        print(T);
```


My answer-

``` pycon
import re
S=int(input());		# Not sure about this line. 
for i in range(S):
      pattern1=re.sub('(?<= )(&&)(?= )', 'and', input())
      pattern2=re.sub('(?<= )(\|\|)(?= )', 'or', pattern1)
      print(pattern2)
```



________________

    PreparePythonRegex and ParsingValidating Roman Numerals

Validating Roman Numerals

``` pycon
regex_pattern = r""	# Do not delete 'r'.
import re
print(str(bool(re.match(regex_pattern, input()))))
```

``` pycon
regex_pattern = r""	# Do not delete 'r'.
# Equals M (1000), D (500), C (100), L (50), X (10), V (5), I (1)
import re
print(str(bool(re.match(regex_pattern, input()))))
```

Discussion Answer-

The engine seems to constrain the answer so you can't add lines etc. So eventually I just put the regex pattern in the quotes. It's a bit cryptic. 

``` pycon
regex_pattern = r"^M{,3}(C(D|M)|D?C{,3})(X(L|C)|L?X{,3})(I(X|V)|(X|V)?I{,3})$"	# Do not delete 'r'.
import re
print(str(bool(re.match(regex_pattern, input()))))
```
____________________________

    PreparePythonRegex and ParsingValidating phone numbers

Validating phone numbers

``` pycon
regex_pattern = r"^(7|8|9){,1}"    # Do not delete 'r'.
import re
# print(str(bool(re.match(regex_pattern, input()))))
S=int(input());        # Not sure about this line. 
for i in range(S):
    if (str(bool(re.match(regex_pattern, input())))):
        print('YES')
    else:
        print('NO')

regex_pattern = r"^7|8|9"    # Do not delete 'r'.
import re
# print(str(bool(re.match(regex_pattern, input()))))
S=int(input());        # Not sure about this line. 
for i in range(S):
    print(input())
    if (str(bool(re.match(regex_pattern, input())))):
        print('YES')
    else:
        print('NO')
```

Discussion Answer-

``` pycon
import re
S=int(input());  
for i in range(S):
    if re.match(r'[789]\d{9}$',input()):   
        print('YES' ) 
    else:  
        print('NO')  
```
____________________

Question- 

    PreparePythonRegex and ParsingValidating and Parsing Email Addresses

Validating and Parsing Email Addresses

``` pycon
import re
S=int(input());  
for i in range(S):
    if re.match(r'[a-zA-Z]\d@[a-zA-Z.]\d.[a-zA-Z]\d{,3}.[a-zA-Z]\d{,2}$',input()):   
        print(input()); 

# Discussion Answer- 

# Failed on 6 out of 7 tests. 

import re
S=int(input())
for i in range(S):
    print(input())
    if (re.match(r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b',input())):   
        print(input())
    else: 
        break

# Passed all 7 tests.

import re
n = int(input())
for _ in range(n):
    x, y = input().split(' ')
    m = re.match(r'<[A-Za-z](\w|-|\.|_)+@[A-Za-z]+\.[A-Za-z]{1,3}>', y)
    if m:
        print(x,y)

import re
n = int(input())
for _ in range(n):
    x, y = input().split(' ')
    if re.match(r'<[A-Za-z](\w|-|\.|_)+@[A-Za-z]+\.[A-Za-z]{1,3}>', y):
        print(x,y)

# Passed 2 out of 7 test cases.

import re
n = int(input())
for _ in range(n):
    x, y = input().split(' ')
    m = re.search(r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b', y)
    if m:
        print(x,y)

# Passed 2 out of 7 test cases. 

import re
n = int(input())
for _ in range(n):
    y = input()
    m = re.search(r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b', y)
    if m:
        print(y)

# Matches all but 1 test case out of 7.

import re
n = int(input())
for _ in range(n):
    x, y = input().split(' ')
    if re.match(r'<[A-Za-z](\w|-|\.|_)+@[A-Za-z]+\.[A-Za-z]+>', y):
        print(x,y)
```
_________________________

###### Question- Hex Color Code

https://www.hackerrank.com/challenges/hex-color-code/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen

Discussion Answer- 

```pycon
import re
if __name__ == "__main__":
    # reg = re.compile(r"(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})")
    # reg = re.compile(r"#[abcdefABCDEF1234567890]{3,}")
    reg = re.compile(r"(:|,| +)(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})\b")
    n = int(input())
    for i in range(n):
        line  = input()
        items = reg.findall(line)
        if items:
            # print(", ".join(str(s) for s in items ))
            # for match in items:
            #   print(items.group())
            for item in items:    
                print( item[1] )

```

Cleaned up-
```pycon
import re
if __name__ == "__main__":
    # reg = re.compile(r"(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})")
    # reg = re.compile(r"#[abcdefABCDEF1234567890]{3,}")
    reg = re.compile(r"(:|,| +)(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})\b")

    n = int(input())
    
    for i in range(n):
        line  = input()
        items = reg.findall(line)

        if items:
            # print(", ".join(str(s) for s in items ))
            # for match in items:
            #   print(items.group())
            for item in items:    
                print( item[1] )

```

Interesting Answer-

```pycon
import re

pattern = r"\.*#([a-f0-9]{6}|[a-f0-9]{3})(=?[;,)])"

for line in range(int(input())):
    match = re.finditer(pattern, input(), flags=re.IGNORECASE)
    for color in match:
        print(color.group()[:-1])
```

```pycon
import re

pattern = r"(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})(=?[;,)])"

for line in range(int(input())):
    match = re.finditer(pattern, input(), flags=re.IGNORECASE)
    for color in match:
        print(color.group()[:-1])
```

```pycon
import re
pattern = r"(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})(=?[;,)])"
n = int(input())
for _ in range(n):
    m = re.match(pattern, input())
    if m:
        print(m)     
```

```pycon
import re
pattern = r"(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})(=?[;,)])"
n = int(input())
for _ in range(n):
    m = re.findall(pattern, input())
    if m:
        print(m)        
```

My Answer-

```pycon
import re
pattern = r"(#[abcdefABCDEF1234567890]{3}|#[abcdefABCDEF1234567890]{6})(=?[;,)])"
for line in range(int(input())):
    match = re.finditer(pattern, input())
    for color in match:
        print(color.group()[:-1])
```
What does [:-1] mean/do in python? - Stack Overflow
https://stackoverflow.com/questions/15535205/what-does-1-mean-do-in-python

_______________________

###### Question- HTML Parser Part 1

https://www.hackerrank.com/challenges/html-parser-part-1/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen

Discussion Answer-

```pycon
from html.parser import HTMLParser
class MyHTMLParser(HTMLParser):
    def handle_starttag(self, tag, attrs):        
        print ('Start :',tag)
        for ele in attrs:
            print ('->',ele[0],'>',ele[1])
            
    def handle_endtag(self, tag):
        print ('End   :',tag)
        
    def handle_startendtag(self, tag, attrs):
        print ('Empty :',tag)
        for ele in attrs:
            print ('->',ele[0],'>',ele[1])
            
MyParser = MyHTMLParser()
MyParser.feed(''.join([input().strip() for _ in range(int(input()))]))

```

Discussion Answer 2- 

```pycon
from html.parser import HTMLParser
class MyHTMLParser(HTMLParser):
    def handle_starttag(self, tag, attrs):        
        print ('Start :',tag)
        for ele in attrs:	# Needs this for loop for the different input values
            print ('->',ele[0],'>',ele[1])
            
    def handle_endtag(self, tag):
        print ('End   :',tag)
        
    def handle_startendtag(self, tag, attrs):
        print ('Empty :',tag)
        for ele in attrs:	# Needs this for loop for the different input values
            print ('->',ele[0],'>',ele[1])
            
MyParser = MyHTMLParser()
for _ in range(int(input())):
    MyParser.feed(input())
```
Interesting Answer- DRY Solution

```pycon
from html.parser import HTMLParser

class MyHTMLParser(HTMLParser):
    def _handler_factory(msg):
        msg = msg.ljust(6) + ':'
        def handler(self, tag, attrs=[]):
            print(msg, tag)
            for a in attrs:
                print("-> %s > %s" % a)
        return handler

    locals().update(zip(
        map("handle_{}tag".format, ("start", "end", "startend")),
        map(_handler_factory, ("Start", "End", "Empty"))
    ))

MyHTMLParser().feed(' '.join(input() for _ in range(int(input()))))

```

Not certain I understood this exercise completely. 

_______________________

###### Question- HTML Parser Part 2

https://www.hackerrank.com/challenges/html-parser-part-2/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen


```pycon
from HTMLParser import HTMLParser

class MyHTMLParser(HTMLParser):
    def handle_comment(self, data):
          print "Comment  :", data
```
```pycon
from HTMLParser import HTMLParser

class MyHTMLParser(HTMLParser):
    def handle_data(self, data):
        print "Data     :", data
```
My Attempt-

```pycon
from HTMLParser import HTMLParser

class MyHTMLParser(HTMLParser):
# If single line comment then 
# If multi line comment then
    def handle_comment(self, data):
	for _ in data:
		if data[1]: # If there is more than one element in data array.
			print ">>> Multi-line Comment"
			for _ in array:
				print data
		else:
			print ">>> Single-line Comment"
			print data

    def handle_data(self, data):
        print ">>> Data"
	print data

```

Discussion Answer-

```pycom
from html.parser import HTMLParser

class MyHTMLParser(HTMLParser):
    def handle_comment(self, comment):
        if '\n' in comment:
            print('>>> Multi-line Comment')
        else:
            print('>>> Single-line Comment')
            
        print(comment)
    
    def handle_data(self, data):
        if data == '\n': return
        print('>>> Data')
        print(data)
  
html = ""       
for i in range(int(input())):
    html += input().rstrip()
    html += '\n'
    
parser = MyHTMLParser()
parser.feed(html)
parser.close()

```
________________________

###### Question- Detect HTML Tags, Attributes and Attribute Values




```pycon
from html.parser import HTMLParser

class MyHTMLParser(HTMLParser):
    def handle_starttag(self, tag, attrs):
        print(tag)

    def handle_endtag(self, tag):
        print(tag)

    def handle_data(self, data):
        print("-> ", )
        print("Encountered some data  :", data)

parser = MyHTMLParser()
parser.feed(input())

```
```pycon
from html.parser import HTMLParser
class MyHTMLParser(HTMLParser):
    def handle_starttag(self, tag, attrs):
        print(tag)
        [print('-> {} > {}'.format(*attr)) for attr in attrs]
        
html = '\n'.join([input() for _ in range(int(input()))])
parser = MyHTMLParser()
parser.feed(html)
parser.close()

```

```pycon
from html.parser import HTMLParser
class MyHTMLParser(HTMLParser):
    def handle_starttag(self, tag, attrs):
        print(tag)
        [print('-> {} > {}'.format(*attr)) for attr in attrs]
        
html = '\n'.join([input() for _ in range(int(input()))])
parser = MyHTMLParser()
parser.feed(html)
parser.close()

```
Test- Code- 

```pycon
from html.parser import HTMLParser
class MyHTMLParser(HTMLParser):
    def handle_starttag(self, tag, attrs):
        print(tag)
        [print(*attr) for attr in attrs]
html = '\n'.join([input() for _ in range(int(input()))])
parser = MyHTMLParser()
parser.feed(html)
parser.close()
```

Test- Output


```pycon

    head

    title

    object

    type application/x-flash

    data your-file.swf

    width 0

    height 0

    param

    name quality

    value high

```
Test- Expected Output

```pycon
    head

    title

    object

    -> type > application/x-flash

    -> data > your-file.swf

    -> width > 0

    -> height > 0

    param

    -> name > quality

    -> value > high
```


_______________________

###### Question- Validating UID


https://www.hackerrank.com/challenges/validating-uid/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen

A valid UID must follow the rules below:

	It must contain at least 2 uppercase English alphabet characters.
	It must contain at least 3 digits (0-9).
	It should only contain alphanumeric characters (a-z, A-Z & 0-9).
	No character should repeat.
	There must be exactly 10 characters in a valid UID.


```pycon

[A-Z|a-z]{2,}
print ("Invalid")
print ("Valid")

import re
for _ in range(int(input())):
    u = ''.join(sorted(input()))
    try:
        assert re.search(r'[A-Z]{2}', u)
        assert re.search(r'\d\d\d', u)
        assert not re.search(r'[^a-zA-Z0-9]', u)
        assert not re.search(r'(.)\1', u)
        assert len(u) == 10
    except:
        print('Invalid')
    else:
        print('Valid')
```

https://docs.python.org/3/library/re.html

.

(Dot.) In the default mode, this matches any character except a newline. If the DOTALL flag has been specified, this matches any character including a newline.

\number

Matches the contents of the group of the same number. Groups are numbered starting from 1. For example, (.+) \1 matches 'the the' or '55 55', but not 'thethe' (note the space after the group). This special sequence can only be used to match one of the first 99 groups. If the first digit of number is 0, or number is 3 octal digits long, it will not be interpreted as a group match, but as the character with octal value number. Inside the '[' and ']' of a character class, all numeric escapes are treated as characters.


(...)

Matches whatever regular expression is inside the parentheses, and indicates the start and end of a group; the contents of a group can be retrieved after a match has been performed, and can be matched later in the string with the \number special sequence, described below. To match the literals '(' or ')', use \( or \), or enclose them inside a character class: [(], [)].

https://www.journaldev.com/24588/python-string-functions

https://www.journaldev.com/23571/python-string-join

https://www.geeksforgeeks.org/try-except-else-and-finally-in-python/

___________________

###### Question- Validating Credit Card Numbers

https://www.hackerrank.com/challenges/validating-credit-card-number/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen


A valid credit card from ABCD Bank has the following characteristics:

► It must start with a 4,5 or 6.
► It must contain exactly 16 digits.
► It must only consist of digits (0-9).
► It may have digits in groups of 4, separated by one hyphen "-".
► It must NOT use any other separator like ' ' , '_', etc.
► It must NOT have or more consecutive repeated digits. 


Answer- First Try-

```pycon
import re
for _ in range(int(input())):
    u = ''.join(input().strip())
    try:
        assert re.search(r'[4,5,6]{1}',u) #
        # assert len(u) == 16 # This doesn't take account of spaces or hyphens. 
	assert re.match(r'(\d{4}-){3}\d{4}$', n) or re.match(r'\d{16}$', n)
        assert not re.search(r'[^0-9]', u)
        assert re.search(r'[0-9]{4}-[0-9]{4}-[0-9]{4}-[0-9]{4}', u)
        assert not re.search(r'(.)\1', u)
    except:
        print('Invalid')
    else:
        print('Valid')
```

```pycon
import re
for _ in range(int(input())):
    u = ''.join(input().strip())
    try:
        assert re.search(r'[4,5,6]{1}',u) #First digit 4,5 or 6- Criteria 1
        # assert len(u) == 16 # Doesn't account spaces hyphens.
        assert re.match(r'(\d{4}-){3}\d{4}', u) or re.match(r'\d{16}', u)#16 digits-Criteria 2345
        #assert not re.search(r'(.)\1', u)
    except:
        print('Invalid')
    else:
        print('Valid')
```
```pycon
import re
for _ in range(int(input())):
    u = ''.join(input().strip())
    try:
        assert re.search(r'[4,5,6]{1}',u) #First digit 4,5 or 6- Criteria 1
        # assert len(u) == 16 # Doesn't account spaces hyphens.
        assert re.match(r'(\d{4}-){3}\d{4}', u) or re.match(r'\d{16}', u)#16 digits-Criteria 2345
        #assert not (re.match(r'([(.)\1]{4}-){3}[(.)\1]{4}', u) or re.match(r'([(.)\1]{4}){4}', u))
        #assert not re.match(r'([(.)\1]{4}){4}', u) # I can't get the last criteria to work Criteria 6. 
    except:
        print('Invalid')
    else:
        print('Valid')
```
Gave up and used discussion answer below. 

```pycon
import re
def check(card):
    if not re.search("^[456]\d{3}(-?\d{4}){3}$",card) or re.search(r"(\d)\1{3}", re.sub("-", "",card)):
        return False
    return True
for i in range(int(input())):
    print("Valid" if check(input()) else "Invalid")
```
_____________________

###### Questions- Validating Postal Codes

https://www.hackerrank.com/challenges/validating-postalcode/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen


regex_integer_in_range should match only integers range from 100000 to 999999 inclusive

regex_alternating_repetitive_digit_pair should find alternating repetitive digits pairs in a given string.

From Discussion Answers- 


```pycon
import re

print(bool(re.match(
    r'^'
    r'(?!.*(.).\1.*(.).\2)'
    r'(?!.*(.)(.)\3\4)'
    r'[1-9]\d{5}'
    r'$', input()
)))
```

```pycon
regex_integer_in_range = r"^[1-9][0-9]{5}$"
regex_alternating_repetitive_digit_pair = r"(\d)(?=.\1)"
```

```pycon
regex_integer_in_range = r"_________"	# Do not delete 'r'.
regex_alternating_repetitive_digit_pair = r"_________"	# Do not delete 'r'.


import re
P = input()

print (bool(re.match(regex_integer_in_range, P)) 
and len(re.findall(regex_alternating_repetitive_digit_pair, P)) < 2)
```

Don't completely understand the information below- from Discussion. 

'''
regex_alternating_repetitive_digit_pair checks that 
it not contains more than one alternating repetitive digit pair
Alternating repetitive digits are digits which repeat immediately after the next digit. In other words, an alternating repetitive digit pair is formed by two equal digits that have just a single digit between them.
'''
regex_alternating_repetitive_digit_pair = r"(\d)(?=.\1)"	

'''
() groups sub-patterns
? matches zero or one occurrence of the pattern left to it.

(?=...)
Matches if ... matches next, but doesn’t consume any of the string. This is called a lookahead assertion. For example, Isaac (?=Asimov) will match 'Isaac ' only if it’s followed by 'Asimov'.

. a period matches any single character (except newline '\n').

\number
Matches the contents of the group of the same number. Groups are numbered starting from 1. For example, (.+) \1 matches 'the the' or '55 55', but not 'thethe'

'''use bignum

______________________

###### Question- Extra Long Factorials

Function Description

Complete the extraLongFactorials function in the editor below. It should print the result and return. 

```pycon
import math
import os
import random
import re
import sys
#
# Complete the 'extraLongFactorials' function below.
#
# The function accepts INTEGER n as parameter.
#

def extraLongFactorials(n):
    # Write your code here
    factorial = 1
    for i in range(1, n+1):
       factorial *= i 
       #print (factorial)
    else:
        print (factorial)
        return factorial
if __name__ == '__main__':
    n = int(input().strip())

    extraLongFactorials(n)

```
________________________

###### Question- Matrix Script

https://www.hackerrank.com/challenges/matrix-script/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen


```pycon
#!/bin/python
import math
import os
import random
import re
import sys
first_multiple_input = raw_input().rstrip().split()
n = int(first_multiple_input[0])
m = int(first_multiple_input[1])
matrix = []
for _ in xrange(n):
    matrix_item = raw_input()
    matrix.append(matrix_item)
    print (matrix)

```

```pycon
matrix = [][]
for _ in xrange(n):
    matrix_item = []
    matrix_item = split_str(raw_input())
    matrix.append(matrix_item)
    print (matrix)


```

Discussion Answer- 

```pycon
import re
import sys

first_multiple_input = input().rstrip().split()

n = int(first_multiple_input[0])

m = int(first_multiple_input[1])

matrix = []

for _ in range(n):
    matrix_item = input()
    matrix.append(matrix_item)

new = ''
for i in range(0,m):
    for j in range(0,n):
        new = new + matrix[j][i]
 
t1 = re.match(r'\W*',new[::-1]).group() 
# https://stackoverflow.com/questions/21617586/reverse-string-string-1-works-but-string0-1-and-others-dont#21617612
# Not sure why but [::-1] seems to be a Python string operation that reverses the order of the string array. 
#For example-  
#txt = "The best things in life are free!"
#print(txt[::-1]) 
# Output- !eerf era efil ni sgniht tseb ehT

t1= t1[::-1]
t2 = re.match(r'\W*',new).group()
s = re.sub('[^0-9a-zA-Z]+', ' ', new).rstrip().lstrip()
k = t2 + s + t1
print((k, t1) [s==''])

```
See https://stackoverflow.com/questions/21617586/reverse-string-string-1-works-but-string0-1-and-others-dont#21617612

See https://www.w3schools.com/python/trypython.asp?filename=demo_default

See https://docs.python.org/3/library/string.html

https://www.w3schools.com/python/python_ref_string.asp

https://www.w3schools.com/python/python_strings.asp

https://www.educba.com/python-string-to-array/

https://docs.python.org/3.8/library/re.html#re.sub

Some demonstration code below

```pycon
import re
string = "999999999 22 333 4444 55555 666666 7777777 88888888 "
## Matching five or more consecutive chars
print (string)
array = re.findall(r"(.)\1{4,}", string)
print (array)
```
```pycon
import re
s1 = 'Blue Berries'
pattern = 'Blue Berries'
for match in re.finditer(pattern, s1):
    s = match.start()
    e = match.end()
    print ('String match "%s" at %d:%d' % (s1[s:e], s, e))
```
Output- String match "Blue Berries" at 0:12

_______________________


###### Question- Any or All

https://www.hackerrank.com/challenges/any-or-all/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen

Condition 1: All the integers in the list are positive.
Condition 2: 5 is a palindromic integer.


```pycon
any([1>0,1==0,1<0])
all(['a'<'b','b'<'c'])

```
```pycon

all(['a'<'b','b'<'c'])
any([1>0,1==0,1<0])
```

Discussion Answer-

I suspect that j == j[::-1] below would fail the palindrome test for N > 100 
ie It works for one and two characters but not for three characters. 
To produce something that works for more than two characters should compare j[::1] == j[::-1] or something similar perhaps?

```pycon
N,n = int(raw_input()),raw_input().split()
print all([int(i)>0 for i in n]) and any([j == j[::-1] for j in n])


```

What does [:-1] mean/do in python? - Stack Overflow
https://stackoverflow.com/questions/15535205/what-does-1-mean-do-in-python

python string [::-1]- Slice Notation

https://stackoverflow.com/questions/21617586/reverse-string-string-1-works-but-string0-1-and-others-dont#21617612


My attempted answer-

```pycon
var1, var2 = int(input()),input().split()
#var= input().rstrip().split()
print (all(int(i)>0 for i in var2) and ) # Need to add the palindrome condition 2- the hints suggests to use "any" method. 

```

```pycon
N,n = int(input()),input().split()
print (all([int(i)>0 for i in n]) and any([j == j[::-1] for j in n]))
```

Use input() not raw_input() for Python 3. 
Also print (var) not print var

Below works- should work for three character palindromes too N > 100. 

```pycon
N,n = int(input()),input().split()
print (all([int(i)>0 for i in n]) and any([j[::1] == j[::-1] for j in n]))
```

___________

###### Question- ginortS (Sorting??)

https://www.hackerrank.com/challenges/ginorts/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen

Your task is to sort the string S in the following manner:

    All sorted lowercase letters are ahead of uppercase letters.
    All sorted uppercase letters are ahead of digits.
    All sorted odd digits are ahead of sorted even digits.

https://www.asciitable.com/
https://www.pythonforbeginners.com/basics/ascii-value-in-python
The ord() function takes the given character as input and returns the ASCII value of the character.

```pycon
S= input()
Out= ""
for _ in S:
    

```

Discussion Answer- 

https://www.hackerrank.com/challenges/ginorts/forum

The sorted function will return the sort as "an array"/ *sorted will return the sort as "a string".

```pycon
order = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1357902468'
print(*sorted(input(), key=order.index), sep='')

```
___________

###### Question- Integers Come In All Sizes

https://www.hackerrank.com/challenges/python-integers-come-in-all-sizes/problem

```pycon
a,b,c,d = (int(input()) for _ in range(4))
A= []
A= input().split
#for i in input():
    #A[i]= input()
#print (A[0], A[1], A[2], A[3])
print (A)
  
'''a,b,c,d = (int(input()) for _ in range(4))
#print ("a= ", a, "b= ", b, "c=", c, "d=", d)
print (pow(a,b)+pow(c,d))'''
#arr = [ int(input()) for i in range(n)]
arr= []
arr = [ int(input()) for i <> ""]


A= []
for i in input():
    A[i]= int(input().split())
    print (A[i])
print ("A = ")
print (A)

```
https://stackoverflow.com/questions/56615312/how-to-take-input-in-array-in-python-3#56624087


Discussion Answer- 

```pycon
a,b,c,d = (int(input()) for _ in range(4))
print (pow(a,b)+pow(c,d))    

```
___________

###### Question- Triangle Quest

https://www.hackerrank.com/challenges/python-quest-1/problem


Discussion Page- 
https://www.hackerrank.com/challenges/python-quest-1/forum

Discussion Answer- 

For those wondering why their solution appears to work but is being marked wrong, this problem doesn't allow string manipulation or additional for loops.

If you're still struggling, here's a hint:
1/9 = .1111111111
2/9 = .2222222222
3/9 = .3333333333

```pycon
for i in range(1,int(input())): #More than 2 lines will result in 0 score. Do not leave a blank line also
    print (i * (10**i - 1)//9)
```
___________

###### Question- Tuples

Date: 28 Dec 2021 

https://www.hackerrank.com/challenges/python-tuples/problem

This question doesn't allow answers in Python 3 only Python 2.  

Discussion Answers-

https://www.hackerrank.com/challenges/python-tuples/forum

I don't understand this question at all. But the code below gives the correct answer. 

```pycon
if __name__ == '__main__':
    n = int(raw_input())
    integer_list = map(int, raw_input().split())
    print(hash(tuple(integer_list)))
```

https://docs.python.org/3.8/library/functions.html#map

map(function, iterable, ...)

    Return an iterator that applies function to every item of iterable, yielding the results. If additional iterable arguments are passed, function must take that many arguments and is applied to the items from all iterables in parallel. With multiple iterables, the iterator stops when the shortest iterable is exhausted. For cases where the function inputs are already arranged into argument tuples, see itertools.starmap().

https://docs.python.org/3.8/library/functions.html#hash

 hash(object)

    Return the hash value of the object (if it has one). Hash values are integers. They are used to quickly compare dictionary keys during a dictionary lookup. Numeric values that compare equal have the same hash value (even if they are of different types, as is the case for 1 and 1.0).

https://docs.python.org/3.8/library/functions.html


class tuple([iterable])

    Rather than being a function, tuple is actually an immutable sequence type, as documented in Tuples and Sequence Types — list, tuple, range.

https://www.tutorialspoint.com/python3/tuple_tuple.htm
The tuple() method converts a list of items into tuples.


_____________

###### Question- List Comprehensions

Date: 28 Dec 2021 

https://www.hackerrank.com/challenges/list-comprehensions/problem

Answer First attempt-

```pycon
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
    for i in x:
        for j in y:
            for k in z:
                #if x+y+z!= n:
               #Create 1D / 3 element array and add it to the output list. 
    for i in y:
        for j in z:
            for k in x:
                #if x+y+z!= n:
                #Create 1D / 3 element array and add it to the output list. 
    for i in z:
        for j in x:
            for k in y:
                #if x+y+z!= n:  
                #Create 1D / 3 element array and add it to the output list. 
    #print output list

```

Discussion Answers-

https://www.hackerrank.com/challenges/list-comprehensions/forum

```pycon
x, y, z, n = (int(raw_input())+1 for _ in range(4))
print [[a,b,c] for a in range(x) for b in range(y) for c in range(z) if a+b+c!=n-1]


listijk = []
for i in range(x + 1):
    for j in range (y + 1):
        for k in range (z + 1):
            if i + j + k != n: #before printing the result, it will exclude the output which 'i' + 'j' + 'k' is the same as 'n'.
                listijk.append([i,j,k])
print(listijk)

# Below passes test case. 

if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
    print ([[a,b,c] for a in range(x+1) for b in range(y+1) for c in range(z+1) if a+b+c!=n])
```

_____________

###### Question- Find the Runner-Up Score

Date: 28 Dec 2021 

https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem

Discussion Answers-

https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/forum

```pycon
if __name__ == '__main__':
    max = max2 = -100 - int(input())
    nums = list(map(int,input().split(' ')))
    for i in range(len(nums)):
        if nums[i] > max2:
            if nums[i] > max:
                max,max2 = nums[i],max
            elif nums[i] < max:
                max2 = nums[i]
    print(max2)      


```

https://www.geeksforgeeks.org/numpy-argsort-in-python/

numpy.argsort() function is used to perform an indirect sort along the given axis using the algorithm specified by the kind keyword. It returns an array of indices of the same shape as arr that that would sort the array.

    Syntax : numpy.argsort(arr, axis=-1, kind=’quicksort’, order=None)

```pycon
a = list(map(int, input().split(' ')))
a.sort()

a = sorted(map(int, input().split(' ')))

# My attempted answer-

if __name__ == '__main__':
    n = int(input())
    arr = map(int, input().split())
    output= sorted(arr)
    #output[n]
    #print (output[n-2])
    maximum= output[n-1]
    for i in reversed (output):
        if output [n-i] != maximum:
             print (output [n-i])
             exit
```


_____________

###### Question- Nested Lists

https://www.hackerrank.com/challenges/nested-list/problem

Discussion Answers-

https://www.hackerrank.com/challenges/nested-list/forum

```pycon
marksheet = []
for _ in range(0,int(input())):
    marksheet.append([input(), float(input())])
second_highest = sorted(list(set([marks for name, marks in marksheet])))[1]
print('\n'.join([a for a,b in sorted(marksheet) if b == second_highest]))


n = int(input())
marksheet = [[input(), float(input())] for _ in range(n)]


n = int(raw_input())
marks = [[raw_input(), float(raw_input())] for i in  xrange(n)]           
scores = sorted({s[1] for s in marks})
result = sorted(s[0] for s in marks if s[1] == scores[1])
print '\n'.join(result)

```

```pycon
if __name__ == '__main__':
    for _ in range(int(input())):
        name = input()
        score = float(input())
        student= [name, score]
        students.append(student)
    print (len(students))
    # Find minimum value of score and remove item from array. 
    # Find minimum value of score and print all names with this score. 
    studsort= sorted(students)
```


_____________

###### Question- Finding the percentage

https://www.hackerrank.com/challenges/finding-the-percentage/problem

Discussion Answers- 

https://www.hackerrank.com/challenges/finding-the-percentage/forum


My Answer-


```pycon
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    #student_marks[query_name]
    # "{:.2f}".format(float)
    print ("{:.2f}".format((student_marks[query_name][0] + student_marks[query_name][1] + student_marks[query_name][2])/3))


print (student_marks)
{'Krishna': [67.0, 68.0, 69.0], 'Arjun': [70.0, 98.0, 63.0], 'Malika': [52.0, 56.0, 60.0]}

```

I wasn't convinced that I understood how to access "student_marks" based on an index. I considered that "student_marks" is like a 2-D array- it appears to be a "dictionary". Some information on dictionaries appears below.  

https://pythonguides.com/python-print-2-decimal-places/
https://www.w3schools.com/python/python_dictionaries.asp
https://docs.python.org/3/tutorial/datastructures.html

Ordered or Unordered?
As of Python version 3.7, dictionaries are ordered. In Python 3.6 and earlier, dictionaries are unordered.
When we say that dictionaries are ordered, it means that the items have a defined order, and that order will not change. Unordered means that the items does not have a defined order, you cannot refer to an item by using an index.

_____________

###### Question- The Captain's Room

https://www.hackerrank.com/challenges/py-the-captains-room/problem

Discussion Answers-

https://www.hackerrank.com/challenges/py-the-captains-room/forum

Solution using sets. 

```pycon
if __name__ == '__main__':
    k, rooms, single, multiple = input(), input().split(), set(), set()
    for room in rooms: single.add(room) if room not in single else multiple.add(room)
    print(single.difference(multiple).pop()) 
```


My attempt-

```pycon
if __name__ == '__main__':
    K = int(input())
    persons_room = list(map(int,input().split(' ')))
    room_count = [] # Should be list of tuples or 2D array 
    for _ in len(persons_room):
        if not room_count[persons_room]:
            room_count.append(persons_room)
            # Put number 1 in the room count column.  
        else:
            # Add 1 to the room count column.
    # Find the column that has a room count of 1.
    print (persons_room)  
    print (room_count) 
```


_____________

###### Question- Check Subset

https://www.hackerrank.com/challenges/py-check-subset/problem

Discussion Answers-

https://www.hackerrank.com/challenges/py-check-subset/forum

```pycon
if __name__ == '__main__':
    #k, rooms, single, multiple = input(), input().split(), set(), set()
    # T, A, A_set, B, B_set
    T = int(input())
    for _ in T:
	A= int(input())
	A_set= input().split()
	B= int(input())
	B_set= input().split()
	print (A_set in B_set)
    #for room in rooms: single.add(room) if room not in single else multiple.add(room)
    #print(single.difference(multiple).pop()) 
```

Tests ok-

```pycon
if __name__ == '__main__':
    T = int(input())
    #print (T)
    for _ in range(T):
        A= input()
        A_set= set(input())
        B= input()
        B_set= set(input())
        #print (A)
        #print (A_set)
        #print (B)
        #print (B_set)
        print (A_set.issubset(B_set))
```

Shorter- Failed on submit.

```pycon
if __name__ == '__main__':
    T = int(input())
    for _ in range(T):
        A, A_set, B, B_set= input(), set(input()), input(), set(input())
        print (A_set.issubset(B_set))

# Fixed with split()

if __name__ == '__main__':
    T = int(input())
    for _ in range(T):
        A, A_set, B, B_set= input(), set(input().split()), input(), set(input().split())
        print (A_set.issubset(B_set))

```
Here is some information on Nested List Comprehensions in Python. Seems to be related to multi-dimensional arrays in Python. A couple of times in the about questions I thought that a better understanding of Multi-D Arrays would come in handy. 
 
https://www.geeksforgeeks.org/nested-list-comprehensions-in-python/

Also see Flatten List example in above link. 

https://docs.python.org/3/library/stdtypes.html#typesseq

https://www.plus2net.com/python/mutable-immutable.php

https://docs.python.org/3/faq/programming.html#faq-multidimensional-list



```pycon
# 3D Array (i, j, k)?
matrix = [[[k for k in range(5)] for j in range(5)] for i in range(5)]
```
>>> print(matrix)
[[[0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4]], [[0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4]], [[0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4]], [[0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4]], [[0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4]]]

>>> matrix[1][1][1]
1
>>> matrix[1][1][0]
0
>>> matrix[1][0][1]
1
>>> matrix[0][0][1]
1
>>> 

_____________

###### Question- Check Strict Superset

https://www.hackerrank.com/challenges/py-check-strict-superset/problem

Discussion Answers-

https://www.hackerrank.com/challenges/py-check-strict-superset/forum


```pycon
A, n  = set(input().split()), int(input())
Other= []
for i in range(n):
    Other[i]= set(input().split())
    print (A_set.issubset(B_set)) 
```

Passed Commit Test but didn't pass all Submit Tests. 

```pycon
A, n  = set(input().split()), int(input())
$##print (n)
Other= []
for i in range(n):
    Other.append(set(input().split()))
    #Other[i]= set(input().split())
    #print (i)
    #print (Other[i])
    print (Other[i].issubset(A))
    '''if not (Other[i].issubset(A))
        print (Other[i].issubset(A))
        break '''
```
Submitted ok. 

```pycon
A, n  = set(input().split()), int(input())
#print (A)
#print (n)
Other= []
result= True
for i in range(n):
    Other.append(set(input().split()))
    #Other[i]= set(input().split())
    #print (i)
    #print (Other[i])
    #print (Other[i].issubset(A))
    if not (Other[i].issubset(A)):  # If Other is not a subset of A- ie False.
        result= Other[i].issubset(A)
        break
print (result)
```
_____________

###### Question- Python Evaluation

https://www.hackerrank.com/challenges/python-eval/problem


Discussion Answers-

https://www.hackerrank.com/challenges/python-eval/forum

Compiled fine. 

```pycon

#print(str(eval(input())))
eval(input())


```

_____________

###### Question- Athlete Sort
https://www.hackerrank.com/challenges/python-sort-sort/problem

Discussion Answers-
https://www.hackerrank.com/challenges/python-sort-sort/forum

```pycon
N, M = map(int, input().split())
rows = [input() for _ in range(N)]
K = int(input())

for row in sorted(rows, key=lambda row: int(row.split()[K])):
    print(row)
```

```pycon
#!/bin/python3

import math
import os
import random
import re
import sys

if __name__ == '__main__':
    nm = input().split()
    n = int(nm[0])
    m = int(nm[1])
    arr = []
    for _ in range(n):
        arr.append(list(map(int, input().rstrip().split())))
    k = int(input())
    for row in sorted(rows, key=lambda row: int(row.split()[K])):
        print(row)
```
I'm not sure what this question is doing. But the code below submits.
The first row shows the number of data rows and columns. 
The last row shows the column number that the data is to be sorted by.  

```pycon
#!/bin/python3

import math
import os
import random
import re
import sys

if __name__ == '__main__':
    N, M = map(int, input().split())
    rows = [input() for _ in range(N)]
    K = int(input())

    for row in sorted(rows, key=lambda row: int(row.split()[K])):
        print(row)
```

Notes- on Lambda, Map, Input() see below. 
https://www.w3schools.com/python/ref_func_map.asp
https://www.geeksforgeeks.org/python-input-methods-competitive-programming/?ref=rp
https://docs.python.org/3.8/library/functions.html#map
https://docs.python.org/3/howto/sorting.html
https://stackoverflow.com/questions/13669252/what-is-key-lambda
https://stackoverflow.com/questions/8966538/syntax-behind-sortedkey-lambda
https://www.programiz.com/python-programming/anonymous-function
https://www.geeksforgeeks.org/python-lambda-anonymous-functions-filter-map-reduce/
https://pythonguides.com/python-anonymous-function/

_____________

###### Question- Default Arguments

https://www.hackerrank.com/challenges/default-arguments/problem

```pycon
class EvenStream(object):
    def __init__(self):
        self.current = 0

    def get_next(self):
        to_return = self.current
        self.current += 2
        return to_return

class OddStream(object):
    def __init__(self):
        self.current = 1

    def get_next(self):
        to_return = self.current
        self.current += 2
        return to_return

def print_from_stream(n, stream=EvenStream()):
    for _ in range(n):
        print(stream.get_next())


queries = int(input())
for _ in range(queries):
    stream_name, n = input().split()
    n = int(n)
    if stream_name == "even":
        print_from_stream(n)
    else:
        print_from_stream(n, OddStream())


```


Discussion Answers-

https://www.hackerrank.com/challenges/default-arguments/forum

<b>not sure I really understand this completely </b>
The line that needs to be added is "stream.__init__()" to reset the stream- class instance- .  

```pycon
class EvenStream(object):
    def __init__(self):
        self.current = 0

    def get_next(self):
        to_return = self.current
        self.current += 2
        return to_return

class OddStream(object):
    def __init__(self):
        self.current = 1

    def get_next(self):
        to_return = self.current
        self.current += 2
        return to_return

def print_from_stream(n, stream=EvenStream()):
    stream.__init__()	# Need to reset the Stream. 
    for _ in range(n):
        print(stream.get_next())


queries = int(input())
for _ in range(queries):
    stream_name, n = input().split()
    n = int(n)
    if stream_name == "even":
        print_from_stream(n)
    else:
        print_from_stream(n, OddStream())


```

Useful links- 
https://stackoverflow.com/questions/46592445/python3-best-way-to-read-unknown-multi-line-input



_____________

###### Question- Triangle Quest 2

https://www.hackerrank.com/challenges/triangle-quest-2/problem


Discussion Answers-
https://www.hackerrank.com/challenges/triangle-quest-2/forum

```pycon
for i in range(0,int(input())): #More than 2 lines will result in 0 score. Do not leave a blank line also
    print ([1, 121, 12321, 1234321, 123454321, 12345654321, 1234567654321, 123456787654321, 12345678987654321, 12345678910987654321][i])

```


_____________

###### Question- Mod Divmod
https://www.hackerrank.com/challenges/python-mod-divmod/problem


```pycon
num= int(input())
den= int(input())
tup= divmod(num, den)
print(tup[0])
print(tup[1])
print(tup)

```

Discussion Answers-
https://www.hackerrank.com/challenges/python-mod-divmod/forum

_____________

###### Question- Power - Mod Power
https://www.hackerrank.com/challenges/python-power-mod-power/problem

Discussion Answers-
https://www.hackerrank.com/challenges/python-power-mod-power/forum

```pycon
a= int(input())
b= int(input())
m= int(input())
print(pow(a,b))
print(pow(a,b,m))

```

_____________

###### Question- String Validators
https://www.hackerrank.com/challenges/string-validators/problem


Answer- 
```pycon
if __name__ == '__main__':
    inpu = input()
    isalnum= False
    isalpha= False
    isdigit= False
    islower= False
    isupper= False

    for i in range(len(inpu)):
        if inpu[i].isalnum():
            isalnum= True
        if inpu[i].isalpha():
            isalpha= True
        if inpu[i].isdigit():
            isdigit= True
        if inpu[i].islower():
            islower= True
        if inpu[i].isupper():
            isupper= True
    print(isalnum)
    print(isalpha)
    print(isdigit)
    print(islower)
    print(isupper)

```
Discussion Answers-
https://www.hackerrank.com/challenges/string-validators/forum

Interesting Discussion Answers-

```pycon
str = raw_input()
print any(c.isalnum()  for c in str)
print any(c.isalpha() for c in str)
print any(c.isdigit() for c in str)
print any(c.islower() for c in str)
print any(c.isupper() for c in str)

# This one is very compact
print "\n".join([str(any(i)) for i in (list(zip(*[[c.isalnum(), c.isalpha(), c.isdigit(), c.islower(), c.isupper()] for c in raw_input()])))])

# Python has a function called any() that returns True if any one of the list elements evals to True.

print(any([0, 1, 0, 0])) # will print True
print(any([0, 0, 0, 0])) # will print False

# This one is similar to my answer
string = raw_input()
l=list(string)
a,b,c,d,e=False,False,False,False,False
for i in l:
    if i.isalnum():
        a=True
    if i.isalpha():
        b=True
    if i.isdigit():
        c=True
    if i.islower():
        d=True
    if i.isupper():https://www.w3schools.com/python/trypython.asp?filename=demo_ref_string_join
        e=True
print a
print b
print c
print d
print e

# I used similar approach, but with a stopper after we found all the cases.

rv = [False,False,False,False,False]
...
for i in range(0,len(s)):
    if rv[0] & rv[1] & rv[2] & rv[3] & rv[4]:
        break # no need to read the whole string if all cases passed
    if not rv[0]:
        rv[0] = s[i].isalnum():
    if not rv[1]:
        ...
```
_____________

###### Question- Text Alignment
https://www.hackerrank.com/challenges/text-alignment/problem


```pycon
#Replace all ______ with rjust, ljust or center. 

thickness = int(input()) #This must be an odd number
c = 'H'

#Top Cone
for i in range(thickness):
    print((c*i).rjust(thickness-1)+c+(c*i).rjust(thickness-1))

#Top Pillars
for i in range(thickness+1):
    print((c*thickness).rjust(thickness*2)+(c*thickness).rjust(thickness*6))

#Middle Belt
for i in range((thickness+1)//2):
    print((c*thickness*5).rjust(thickness*6))    

#Bottom Pillars
for i in range(thickness+1):
    print((c*thickness).rjust(thickness*2)+(c*thickness).rjust(thickness*6))    

#Bottom Cone
for i in range(thickness):
    print(((c*(thickness-i-1)).rjust(thickness)+c+(c*(thickness-i-1)).rjust(thickness)).rjust(thickness*6))

```
Discussion Answers-
https://www.hackerrank.com/challenges/text-alignment/forum

```pycon
#Replace all ______ with rjust, ljust or center. 

thickness = int(input()) #This must be an odd number
c = 'H'

#Top Cone
for i in range(thickness):
    print((c*i).rjust(thickness-1)+c+(c*i).ljust(thickness-1))

#Top Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))

#Middle Belt
for i in range((thickness+1)//2):
    print((c*thickness*5).center(thickness*6))    

#Bottom Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))    

#Bottom Cone
for i in range(thickness):
    print(((c*(thickness-i-1)).rjust(thickness)+c+(c*(thickness-i-1)).ljust(thickness)).rjust(thickness*6))
```

See solution / interesting links- 
https://programs.programmingoneonone.com/2021/01/hackerrank-text-alignment-solution-python.html
https://www.w3schools.com/python/trypython.asp?filename=demo_ref_string_rjust

_____________

###### Question- Text Wrap
https://www.hackerrank.com/challenges/text-wrap/problem

Discussion Answers- 
https://www.hackerrank.com/challenges/text-wrap/forum

```pycon
import textwrap

def wrap(string, max_width):
    return "\n".join(textwrap.wrap(string, max_width))    # The "return" variable is the piece that needs to be modified. 

if __name__ == '__main__':
    string, max_width = input(), int(input())
    result = wrap(string, max_width)
    print(result)
```

Interesting solution-
```pycon
def wrap(string, max_width):
    return "\n".join([string[i:i+max_width] for i in range(0, len(string), max_width)])
```
Links-
https://www.w3schools.com/python/trypython.asp?filename=demo_ref_string_join
https://docs.python.org/3/library/textwrap.html
https://docs.python.org/3/library/textwrap.html#textwrap.TextWrapper.wrap

_____________

###### Question- Designer Door Mat
https://www.hackerrank.com/challenges/designer-door-mat/problem 


```pycon
N, M= input().split()
N, M= int(N), int(M)
print (N, M)
for i in range(M-3/2):


```
Discussion Answers-
https://www.hackerrank.com/challenges/designer-door-mat/forum

```pycon
n, m = map(int,input().split())
pattern = [('.|.'*(2*i + 1)).center(m, '-') for i in range(n//2)]
print('\n'.join(pattern + ['WELCOME'.center(m, '-')] + pattern[::-1]))



N, M = map(int,input().split())
for i in range(1,N,2): 
    print((i * ".|.").center(M, "-"))
print("WELCOME".center(M,"-"))
for i in range(N-2,-1,-2): 
    print((i * ".|.").center(M, "-"))

```

_____________

###### Question- String Formatting
https://www.hackerrank.com/challenges/python-string-formatting/problem

Answers-

```pycon
def print_formatted(number):
    # your code goes here
    for i in range(1, number +1):
        print (i, oct(i).replace("0o", ""), hex(i).replace("0x", "") , (bin(i).replace("0b", "")).rjust(5))     
if __name__ == '__main__':
    n = int(input())
    print_formatted(n)


```
Discussion Answers-
https://www.hackerrank.com/challenges/python-string-formatting/forum

```pycon

n = int(raw_input())
width = len("{0:b}".format(n))
for i in xrange(1,n+1):
  print "{0:{width}d} {0:{width}o} {0:{width}X} {0:{width}b}".format(i, width=width)


STDIN = int(raw_input())
w = len(str(bin(STDIN)).replace('0b',''))
for i in xrange(1, STDIN+1):
    b = bin(int(i)).replace('0b','').rjust(w, ' ')
    o = oct(int(i)).replace('0','', 1).rjust(w, ' ')
    h = hex(int(i)).replace('0x','').upper().rjust(w, ' ')
    j = str(i).rjust(w, ' ')
    print j, o, h, b

#Compiled ok. 

def print_formatted(number):
    # your code goes here
    #STDIN = int(input())
    # print (STDIN)
    w = len(str(bin(number)).replace('0b',''))
    for i in range(1, number+1):
        b = bin(int(i)).replace('0b','').rjust(w, ' ')
        o = oct(int(i)).replace('0o','', 1).rjust(w, ' ')
        h = hex(int(i)).replace('0x','').upper().rjust(w,  ' ')
        j = str(i).rjust(w, ' ')
        print (j, o, h, b)

if __name__ == '__main__':
    n = int(input())
    print_formatted(n)

```

_____________

###### Question- Alphabet Rangoli
https://www.hackerrank.com/challenges/alphabet-rangoli/problem

```pycon



```


Discussion Answers-
https://www.hackerrank.com/challenges/alphabet-rangoli/forum

```pycon
import string
alpha = string.ascii_lowercase

n = int(input())
L = []
for i in range(n):
    s = "-".join(alpha[i:n])
    L.append((s[::-1]+s[1:]).center(4*n-3, "-"))
print('\n'.join(L[:0:-1]+L))



def print_rangoli(n):
    from string import ascii_lowercase as chars
    heap = [(('-'.join(chars[i:n])[::-1]+'-'.join(chars[i:n])[1:])).center(4*n-3, '-')for i in range(n)]
    print(*(heap[::-1]+heap[1:]), sep="\n")



def print_rangoli(size):
    width = 4 * size - 3
    alpha = string.ascii_lowercase
    for i in list(range(size))[::-1] + list(range(1, size)):
        print('-'.join(alpha[size-1:i:-1] + alpha[i:size]).center(width, '-'))


def print_rangoli(size):
    myStr = 'abcdefghijklmnopqrstuvwxyz'[0:size]
    
    for i in range(size-1, -size, -1):
        x = abs(i)
        if x >= 0:
            line = myStr[size:x:-1]+myStr[x:size]
            print ("--"*x+ '-'.join(line)+"--"*x)


def print_rangoli(size):
    alp = 'abcdefghijklmnopqrstuvwxyz'
    for i in range(size-1,-size,-1):
        temp = '-'.join(alp[size-1:abs(i):-1]+alp[abs(i):size])
        print(temp.center(4*size-3,'-'))
          
if __name__ == '__main__':
    n = int(input())
    print_rangoli(n)


import string

size = int(input())
alphabet = string.ascii_lowercase

for i in range(size - 1, 0, -1):
    row = ["-"] * (size * 2 - 1)
    for j in range(0, size - i):
        row[size - 1 - j] = alphabet[j + i]
        row[size - 1 + j] = alphabet[j + i]
    print("-".join(row))

for i in range(0, size):
    row = ["-"] * (size * 2 - 1)
    for j in range(0, size - i):
        row[size - 1 - j] = alphabet[j + i]
        row[size - 1 + j] = alphabet[j + i]
    print("-".join(row))


import string
N = int(input())
alphabet = string.ascii_lowercase

for i in range(N-1, -N, -1):
    row = ["-"]*(4*N-3)
    for j in range(0, N - abs(i)):
        row[2*(N-1+j)] = alphabet[abs(i)+j]
        row[2*(N-1-j)] = alphabet[abs(i)+j]
    print("".join(row))


# instead of typing the alphabet use:
import string
alphabet = string.ascii_lowercase


l = [chr(96+i) for i in range(size, 0, -1)]
{print(('-'.join(l[:i]+l[i::-1])).center(size*4-3, '-')) for i in list(range(size))+list(range(size-2, -1, -1))}



# Syntax
# string.center(string_length, fill_character_default_space)


import string
alpha = string.ascii_lowercase

n = 7
L = []
for i in range(n):
    s = "-".join(alpha[i:n])
    L.append((s[::-1]+s[1:]).center(4*n-3, " ")) # The reason for the 4*n-3 value is because the line needs to be of length approximately 7x2 to include all the characters plus 7x2 to account for the whitespace characters- in this case '-'
print('\n'.join(L[:0:-1]+L))



import string
def print_rangoli(size):
    # your code goes here
    alpha = string.ascii_lowercase
    L = []
    for i in range(size):
        s = "-".join(alpha[i:size])
        L.append((s[::-1]+s[1:]).center(4*size-3, "-")) # The reason for the 4*n-3 value is because the line needs to be of length approximately 7x2 to include all the characters plus 7x2 to account for the whitespace characters- in this case '-'
    print('\n'.join(L[:0:-1]+L))
if __name__ == '__main__':
    n = int(input())
    print_rangoli(n)

```

Links- 
https://www.w3schools.com/python/ref_string_center.asp
https://realpython.com/python-print/
https://realpython.com/python-f-strings/

_____________

###### Question- 


Discussion Answers-


```pycon
#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the solve function below.
def solve(s):
    for x in s[:].split():
        s = s.replace(x, x.capitalize())
    return s
    

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    s = input()

    result = solve(s)

    fptr.write(result + '\n')

    fptr.close()


```


_____________

###### Question- The Minion Game

https://www.hackerrank.com/challenges/the-minion-game/problem

Discussion Answers-
https://www.hackerrank.com/challenges/the-minion-game/forum

```pycon
def minion_game(string):
    # your code goes here
        #s = raw_input()

    vowels = 'AEIOU'

    kevsc = 0
    stusc = 0
    for i in range(len(s)):
        if s[i] in vowels:
            kevsc += (len(s)-i)
        else:
            stusc += (len(s)-i)

    if kevsc > stusc:
        print ("Kevin", kevsc)
    elif kevsc < stusc:
        print ("Stuart", stusc)
    else:
        print ("Draw")

if __name__ == '__main__':
    s = input()
    minion_game(s)
```


_____________

###### Question- Merge the Tools!
https://www.hackerrank.com/challenges/merge-the-tools/problem

Discussion Answers-
https://www.hackerrank.com/challenges/merge-the-tools/forum

https://www.thepoorcoder.com/hackerrank-merge-the-tools-solution/


```pycon
# I Couldn't work out completely what they were trying to say in the question- but the below code worked.

def merge_the_tools(string, k):
    # your code goes here
    for i in range(0,len(string), k):
        #slice string upto k characters
        line = string[i:i+k]
        seen = set()
        for i in line:
            #only print if we haven't already seen this character
            if i not in seen:
                print(i,end="")
                seen.add(i)
        #prints a new line
        print()
if __name__ == '__main__':
    string, k = input(), int(input())
    merge_the_tools(string, k)

```

_____________

###### Question- Arrays- Date 17/03/2022
https://www.hackerrank.com/challenges/np-arrays/problem


Discussion Answers-
https://www.hackerrank.com/challenges/np-arrays/forum

```pycon
import numpy

def arrays(arr):
    # complete this function
    # use numpy.array
    for i in len(arr):
        result[i]= arr[len(arr)-i]
    return result
    

arr = input().strip().split(' ')
result = arrays(arr)
print(result)


______________


import numpy

def arrays(arr):
    # complete this function
    # use numpy.array
    for i in range(0, len(arr)):
        array[i]= arr[len(arr)-i-1]
    return array
    

arr = input().strip().split(' ')
result = arrays(arr)
print(result)

________________

import numpy

def arrays(arr):
    # complete this function
    # use numpy.array
    #print (arr)
    #array= []
    # for i in range(0, len(arr)-1):
        #print ("i= ", i)
        #print ("len(arr)-1 = ", len(arr)-1)
        #print (arr[len(arr)-i-1])
        # my_array = np.asarray(my_list)
        #array= numpy.array(arr)
        # data.astype(float)
        #array.astype(float)
        # print(array)
        # result = arr[::-1]
        # array[i]= arr[len(arr)-i-1]
        # print (L1[-1])
    #return array[::-1]
    return(numpy.array(arr[::-1], float))    
    

arr = input().strip().split(' ')
result = arrays(arr)
print(result)

_______________


# From discussion answers.

import numpy

def arrays(arr):
    # complete this function
    # use numpy.array
    return(numpy.array(arr[::-1], float))    
    

arr = input().strip().split(' ')
result = arrays(arr)
print(result)

```
________






_____________

###### Question- Shape and Reshape- Date 09/04/2022
https://www.hackerrank.com/challenges/np-shape-reshape/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-shape-reshape/forum

```pycon
# My Answer
import numpy
array= list(map(int,input().split()))
print (numpy.reshape(array,(3,3)))

# Other answers
import numpy;print(numpy.reshape(numpy.array(list(map(int,input().split()))),(3,3)))

```




____________

###### Question- Transpose and Flatten- Date 20220410
https://www.hackerrank.com/challenges/np-transpose-and-flatten/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-transpose-and-flatten/forum

```pycon
# Solution
import numpy
narr = numpy.array([input().split() for _ in range(int(input().split()[0]))],int)
print (narr.transpose())
print (narr.flatten())


# Another solution
import numpy
from sys import stdin
array = []
input()
p = numpy.array([line.split() for line in stdin], int)
print(p.transpose())
print(p.flatten())


```


_____________

###### Question- np-concatenate
https://www.hackerrank.com/challenges/np-concatenate/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-concatenate/forum

```pycon
import numpy
a, b, c = map(int,input().split())
array_1 = numpy.array([input().split() for _ in range(a)],int)
array_2 = numpy.array([input().split() for _ in range(b)],int)
print (numpy.concatenate((array_1, array_2), axis = 0)) 

```

_____________

###### Question- np-zeros-and-ones
https://www.hackerrank.com/challenges/np-zeros-and-ones/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-zeros-and-ones/forum

```pycon
nums = tuple(map(int, input().split()))
print (numpy.zeros(nums, dtype = numpy.int))
print (numpy.ones(nums, dtype = numpy.int))
```

My Answer- Failed Submit
```pycon
import numpy
a, b, c = map(int,input().split())
print (numpy.zeros((a, b, c), dtype=int))
print (numpy.ones((a, b, c), dtype=int))

import numpy
nums = tuple(map(int, input().split()))
print (numpy.zeros(nums, dtype = int))
print (numpy.ones(nums, dtype = int))


```
_____________

###### Question- np-eye-and-identity
https://www.hackerrank.com/challenges/np-eye-and-identity/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-eye-and-identity/forum

```pycon
import numpy
N, M = map(int,input().split())
print numpy.eye(N, M)

import numpy
numpy.set_printoptions(legacy= '1.13')
N, M = map(int,input().split())
print (numpy.eye(N, M, dtype = int))

# Answer
import numpy
numpy.set_printoptions(legacy= '1.13')
N, M = map(int,input().split())
print (numpy.eye(N, M))

```

_____________

###### Question- np-array-mathematics
https://www.hackerrank.com/challenges/np-array-mathematics/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-array-mathematics/forum

```pycon
import numpy
n, m = map(int,input().split())  # eg. 1 4
# print (n, m)
#a, b= map(array,input().split())
# Don't fully understand the line below- the range(2) bit. Could have an issue if it wasn't a 1xM array?
a, b = (numpy.array([input().split() for _ in range(n)], dtype=int) for _ in range(2))   # 1 2 3 4, 5 6 7 8
# print (a,b)
print (numpy.add(a, b))       
print (numpy.subtract(a, b))   
print (numpy.multiply(a, b))  
print (numpy.floor_divide(a, b))  
print (numpy.mod(a, b))  
print (numpy.power(a, b))



```

_____________

###### Question- floor-ceil-and-rint
https://www.hackerrank.com/challenges/floor-ceil-and-rint/problem

Discussion Answers-
https://www.hackerrank.com/challenges/floor-ceil-and-rint/forum

```pycon

import numpy
A = map(int,input().split())

# Discussion Solution
import numpy
numpy.set_printoptions(sign=' ')
a = numpy.array(input().split(),float)
print(numpy.floor(a))
print(numpy.ceil(a))
print(numpy.rint(a))

```
_____________

###### Question- np-sum-and-prod
https://www.hackerrank.com/challenges/np-sum-and-prod/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-sum-and-prod/forum

```pycon
import numpy
n, m = map(int,input().split())  
a = numpy.array([input().split() for _ in range(n)], dtype=int)
b= numpy.sum(a, axis = 0)
print (b)
print (b[0] * b[1])

#print (numpy.prod(a, axis = 0))

# Cleaned up
import numpy
n, m = map(int,input().split())  
a = numpy.array([input().split() for _ in range(n)], dtype=int)
#print (a)
b= numpy.sum(a, axis = 0)
#print (b)
print (b[0] * b[1])

# Fails one of the tests- probably because not 2x2 matrix. Try again. 
import numpy
n, m = map(int,input().split())  
a = numpy.array([input().split() for _ in range(n)], dtype=int)
#print (a)
b= numpy.sum(a, axis = 0)
#print (b)
print (numpy.prod(b, axis = 0))


```
_____________

###### Question- np-min-and-max
https://www.hackerrank.com/challenges/np-min-and-max/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-min-and-max/forum

```pycon
import numpy
n, m = map(int,input().split())  
a = numpy.array([input().split() for _ in range(n)], dtype=int)
b= numpy.min(a, axis = 1)
#print (b)
print (numpy.max(b, axis = 0))
```
_____________

###### Question- np-mean-var-and-std
https://www.hackerrank.com/challenges/np-mean-var-and-std/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-mean-var-and-std/forum

```pycon
import numpy
#numpy.set_printoptions(legacy='1.13')
# numpy.set_printoptions(legacy='1.13', sign= ' ')
# numpy.set_printoptions(sign=' ')
n, m = map(int,input().split())  
a = numpy.array([input().split() for _ in range(n)], dtype=int)
print (numpy.mean(a, axis = 1))
print (numpy.var(a, axis = 0))
#print (numpy.std(a, axis = None))
print(numpy.round(numpy.std(a, axis=None), 11))
```
_____________

###### Question- 
https://www.hackerrank.com/challenges/np-dot-and-cross/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-dot-and-cross/forum

```pycon
import numpy
N= int(input())  
#A = (numpy.array([input().split() for _ in range(N)], dtype=int) for _ in range(N))
#B = (numpy.array([input().split() for _ in range(N)], dtype=int) for _ in range(N))
#a, b = (numpy.array([input().split() for _ in range(n)], dtype=int) for _ in range(2))
A= numpy.array([list(map(int,input().split())) for _ in range(N)])
B= numpy.array([list(map(int,input().split())) for _ in range(N)])
#print (A)
#print (B)
print (numpy.cross(A, B))

#Discussion Solution- Need to read up on Dot / Cross Product to be sure that I understand the calculation.  
import numpy
N= int(input())  
A= numpy.array([list(map(int,input().split())) for _ in range(N)])
B= numpy.array([list(map(int,input().split())) for _ in range(N)])
#a, b = (numpy.array([input().split() for _ in range(n)], dtype=int) for _ in range(2))
print (numpy.dot(A, B))
```
_____________

###### Question- np-inner-and-outer
https://www.hackerrank.com/challenges/np-inner-and-outer/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-inner-and-outer/forum

```pycon

# Discussion Answer
import numpy
A= numpy.array(input().split(),int)
B= numpy.array(input().split(),int)
#print (A)
#print (B)
print (numpy.inner(A, B))
print (numpy.outer(A, B))

```
_____________

###### Question- 
https://www.hackerrank.com/challenges/np-polynomials/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-polynomials/forum

```pycon
import numpy
P= numpy.array(input().split(),float)
x= int(input())  
#print (P)
#print (x)
print (numpy.polyval(P, x))
```
_____________

###### Question- 
https://www.hackerrank.com/challenges/np-linear-algebra/problem

Discussion Answers-
https://www.hackerrank.com/challenges/np-linear-algebra/forum

```pycon
import numpy
N= int(input())
A = numpy.array([input().split() for _ in range(N)], dtype=float)
#print (N)
#print (A)
print (numpy.round(numpy.linalg.det(A), 2))
```
_____________

###### Question- 
https://www.hackerrank.com/challenges/py-set-intersection-operation/problem

Discussion Answers-


```pycon
n= int(input())
nroll = set(input().split())
b= int(input())
broll = set(input().split())
print (len(nroll.intersection(broll)))
```
_____________

###### Question- 
https://www.hackerrank.com/challenges/py-set-difference-operation/problem

Discussion Answers-


```pycon
n= int(input())
nroll = set(input().split())
b= int(input())
broll = set(input().split())
print (len(nroll.difference(broll)))
```
_____________

###### Question- 
https://www.hackerrank.com/challenges/py-set-symmetric-difference-operation/problem

Discussion Answers-


```pycon
# Enter your code here. Read input from STDIN. Print output to STDOUT
n= int(input())
nroll = set(input().split())
b= int(input())
broll = set(input().split())
print (len(nroll.symmetric_difference(broll)))
```
_____________

###### Question- 
https://www.hackerrank.com/challenges/py-set-mutations/problem

Discussion Answers-
https://www.hackerrank.com/challenges/py-set-mutations/forum

```pycon
# Discussion Answer
# Enter your code here. Read input from STDIN. Print output to STDOUT
m = int(input())
A = set(map(int, input().split(" ")))
n = int(input())

for i in range(n):
    cmd, args = input().split(" ")
    B = set(map(int, input().split(" ")))
    eval('A.'+cmd+'(B)')

print (sum(A))


```
_____________

###### Question- 
https://www.hackerrank.com/challenges/re-split/problem

Discussion Answers-
https://www.hackerrank.com/challenges/re-split/forum


```pycon
regex_pattern = r"[,.]+"	# Do not delete 'r'.

import re
print("\n".join(re.split(regex_pattern, input())))
```
_____________

###### Question- simple-array-sum
https://www.hackerrank.com/challenges/simple-array-sum/problem

Discussion Answers-

```pycon
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'simpleArraySum' function below.
#
# The function is expected to return an INTEGER.
# The function accepts INTEGER_ARRAY ar as parameter.
#

def simpleArraySum(ar):
    # Write your code here
    sum = 0
    for i in range(len(ar)):
        sum = sum + int(ar[i])
    return sum

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    ar_count = int(input().strip())

    ar = list(map(int, input().rstrip().split()))

    result = simpleArraySum(ar)

    fptr.write(str(result) + '\n')

    fptr.close()


```
_____________

###### Question- reduce-function
https://www.hackerrank.com/challenges/reduce-function/problem

Discussion Answers-
https://www.hackerrank.com/challenges/reduce-function/forum

```pycon
from fractions import Fraction
from functools import reduce

def product(fracs):
    t = reduce(lambda x, y : x * y, fracs)
    # complete this line with a reduce statement
    # reduce(operator.mul , fracs) 
    # reduce(lambda x, y : x * y, fracs)
    return t.numerator, t.denominator

if __name__ == '__main__':
    fracs = []
    for _ in range(int(input())):
        fracs.append(Fraction(*map(int, input().split())))
    result = product(fracs)
    print(*result)
```
Notes- Probably need to go over this example again- it's interesting how the fraction interacts with reduce. 

_____________

###### Question- most-commons
https://www.hackerrank.com/challenges/most-commons/problem

Discussion Answers-
https://www.hackerrank.com/challenges/most-commons/forum


```pycon
#!/bin/python3

import math
import os
import random
import re
import sys
from collections import Counter


if __name__ == '__main__':
    s = input()
    #print (s)
    c = Counter(sorted(s))
    for i in c.most_common(3):
        print(*i) 
```
Notes- I think that the problem writer was looking to get the solution using Regular Expressions- based on the includes- not using "Counter". I probably need to review the above code so I understand it better. This problem was worth 30 Points- compared with most that are only worth 10 points. 


_____________

###### Question- py-set-add
https://www.hackerrank.com/challenges/py-set-add/problem

Discussion Answers-
https://www.hackerrank.com/challenges/py-set-add/forum


```pycon
# Enter your code here. Read input from STDIN. Print output to STDOUT
N= int(input())
s= set()
for _ in range(N):
    s.add(input())
print(len(s))

#One line answer
#print(len(set([str(input()) for x in range(int(input()))])))
```
Notes- Should review the one line answer above.

_____________

###### Question- py-set-discard-remove-pop
https://www.hackerrank.com/challenges/py-set-discard-remove-pop/problem

Discussion Answers-
https://www.hackerrank.com/challenges/py-set-discard-remove-pop/forum


```pycon
# First attempt
command = set()
n = int(input())
s = set(map(int, input().split()))
N = int(input())
for _ in range(N):
    command.add(input())
# command = set(map(int, input().split()))

print (n)
print (s)
print (N)
print (command)

for i in range(N):
    exec(command[i]o.s)
    eval("s."+command[i]+"("+args+")")

print(len(s))
'''
try:

    # Instruction

except KeyError:

    # Instruction
'''
# Discussion Answer-
n = int(input())
s = set(map(int, input().split()))
N = int(input())
for _ in range(N):
    command = input().split()
    cmd  = command[0]
    args = ""
    if len(command)>1 :
        args = command[1]        
    eval("s."+cmd+"("+args+")")
print(sum(s))

```
Notes- 


_____________

###### Question- py-set-union
https://www.hackerrank.com/challenges/py-set-union/problem

Discussion Answers- 
https://www.hackerrank.com/challenges/py-set-union/forum


```pycon

# Enter your code here. Read input from STDIN. Print output to STDOUT
n= int(input())
nroll= set(map(int, input().split()))
b= int(input())
broll= set(map(int, input().split()))
print (len(nroll|broll))

```
Notes- 

_____________

###### Question- decorators-2-name-directory
https://www.hackerrank.com/challenges/decorators-2-name-directory/problem

Discussion Answers-
https://www.hackerrank.com/challenges/decorators-2-name-directory/forum


```pycon
import operator

def person_lister(f):
    def inner(people):
        # complete the function
        return map(f, sorted(people, key=lambda x: x[2]))
    return inner

@person_lister
def name_format(person):
    return ("Mr. " if person[3] == "M" else "Ms. ") + person[0] + " " + person[1]

if __name__ == '__main__':
    people = [input().split() for i in range(int(input()))]
    print(*name_format(people), sep='\n')

```
```pycon
import operator

def person_lister(f):
    def inner(people):
        # complete the function
        #return map(f, sorted(people, key=lambda x: x[2]))
        return map(f, sorted([[e[0], e[1], int(e[2]), e[3]] for e in people], key=operator.itemgetter(2)))
    return inner

@person_lister
def name_format(person):
    return ("Mr. " if person[3] == "M" else "Ms. ") + person[0] + " " + person[1]

if __name__ == '__main__':
    people = [input().split() for i in range(int(input()))]
    print(*name_format(people), sep='\n')
```

Notes- The second map statement corresponds with the problem question better.  

_____________

###### Question- symmetric-difference
https://www.hackerrank.com/challenges/symmetric-difference/problem

Discussion Answers-
https://www.hackerrank.com/challenges/symmetric-difference/forum


```pycon
a,b=(int(input()),input().split())
c,d=(int(input()),input().split())
x=set(b)
y=set(d)
p=y.difference(x)
q=x.difference(y)
r=p.union(q)
print ('\n'.join(sorted(r, key=int)))


# https://www.w3schools.com/python/trypython.asp?filename=demo_ref_sorted4
a = ("1", "2", "3", "4", "10", "9", "8", "7")
x = sorted(a, key= int, reverse=True)
print(x)


a = ("1", "2", "3", "4", "10", "9", "8", "7")
b = set(a)
x = sorted(a, key= int)
print(x)

# Short version of code. 

a,b=(int(input()),input().split())
c,d=(int(input()),input().split())
x, y= set(b), set(d)
print ('\n'.join(sorted((y.difference(x)).union(x.difference(y)), key=int)))

```
Notes- 
https://www.learnpythonwithrune.org/sort-a-python-list-with-string-of-integers-or-a-mixture/


_____________

###### Question- no-idea
https://www.hackerrank.com/challenges/no-idea/problem

Discussion Answers-
https://www.hackerrank.com/challenges/no-idea/forum


```pycon
# Attempt- Passed one test but failed all the others
n, m= input().split()
n_array= input().split()
a_set= set(input())
b_set= set(input())
h= 0
'''
for i in range(len(n)):
    if n[i] in a_set:
        h+= 1
        #print (h)
    elif n[i] in b_set:
        h-= 1   
        #print (h) 
'''        
#, input()
#print (n, m)
#print (n_array)
#print (a_set)
#print (b_set)
#print(h)
print(sum((i in like) - (i in dislike) for i in array))
print(sum((i in a_set) - (i in b_set) for i in n_array))


#Discussion answer
_ = input()
array = input().split()
like = set(input().split())
dislike = set(input().split())
print(sum((i in like) - (i in dislike) for i in array))


# Second attempt- Passed 3 tests failed the rest. 
n, m= input().split()
n_array= input().split()
a_set= set(input().split())
b_set= set(input().split())
h= 0
'''
for i in range(len(n)):
    if n[i] in a_set:
        h+= 1
        #print (h)
    elif n[i] in b_set:
        h-= 1   
        #print (h) 
'''        
#, input()
#print (n, m)
#print (n_array)
#print (a_set)
#print (b_set)
#print(h)
#print(sum((i in like) - (i in dislike) for i in array))
print(sum((i in a_set) - (i in b_set) for i in n_array))


```
Notes- 

_____________

###### Question- class-1-dealing-with-complex-numbers
https://www.hackerrank.com/challenges/class-1-dealing-with-complex-numbers/problem

Discussion Answers-
https://www.hackerrank.com/challenges/class-1-dealing-with-complex-numbers/forum


```pycon
# First attempt using discussion answers. 

class Complex(complex):
    def __add__(self, no):
        return Complex(complex.__add__(self, no))

    def __sub__(self, no):
        return Complex(complex.__sub__(self, no))

    def __mul__(self, no):
        return Complex(complex.__mul__(self, no))

    def __truediv__(self, no):
        return Complex(complex.__truediv__(self, no))

    def mod(self):
        return Complex(complex.__abs__(self))

    def __str__(self):
        return '{0.real:.2f}{0.imag:+.2f}i'.format(self)

# Second attempt. 
# Apparently need to use truediv rather than div in Python3. Otherwise it works. 

class Complex(object):
    def __init__(self, real, imag):
        self.real = real
        self.imag = imag
    def __add__(self, no):        
        x=complex(self.real, self.imag)+complex(no.real, no.imag)
        return Complex(x.real, x.imag).__str__()
    def __sub__(self, no):
        x=complex(self.real, self.imag)-complex(no.real, no.imag)
        return Complex(x.real, x.imag).__str__()
    def __mul__(self, no):
        x=complex(self.real, self.imag)*complex(no.real, no.imag)
        return Complex(x.real, x.imag).__str__()
    def __div__(self, no):
        x=complex(self.real, self.imag)/complex(no.real, no.imag)
        return Complex(x.real, x.imag).__str__()
    def mod(self):
        return Complex(abs(complex(self.real, self.imag)), 0)
    def __str__(self):
        if self.imag == 0:
            result = "%.2f+0.00i" % (self.real)
        elif self.real == 0:
            if self.imag >= 0:
                result = "0.00+%.2fi" % (self.imag)
            else:
                result = "0.00-%.2fi" % (abs(self.imag))
        elif self.imag > 0:
            result = "%.2f+%.2fi" % (self.real, self.imag)
        else:
            result = "%.2f-%.2fi" % (self.real, abs(self.imag))
        return result

# Failed on test 5. 

class Complex(complex):
    def __add__(self, no):
        return Complex(complex.__add__(self, no))

    def __sub__(self, no):
        return Complex(complex.__sub__(self, no))

    def __mul__(self, no):
        return Complex(complex.__mul__(self, no))

    def __truediv__(self, no):
        return Complex(complex.__truediv__(self, no))

    def mod(self):
        return Complex(complex.__abs__(self))

    def __str__(self):
        return '{0.real:.2f}{0.imag:+.2f}i'.format(self)



# Successfully submitted. 
# I went back to the __str__ method that came with the original script and 
# commented out the one that came with the discussion. 
# After passing the tests it seems that you only need to fix the five arithmetic methods 
# and change object to complex in the class header. 

import math

class Complex(complex):
    def __add__(self, no):
        return Complex(complex.__add__(self, no))

    def __sub__(self, no):
        return Complex(complex.__sub__(self, no))

    def __mul__(self, no):
        return Complex(complex.__mul__(self, no))

    def __truediv__(self, no):
        return Complex(complex.__truediv__(self, no))

    def mod(self):
        return Complex(complex.__abs__(self))

    '''def __str__(self):
        return '{0.real:.2f}{0.imag:+.2f}i'.format(self)'''
    def __str__(self):
        if self.imag == 0:
            result = "%.2f+0.00i" % (self.real)
        elif self.real == 0:
            if self.imag >= 0:
                result = "0.00+%.2fi" % (self.imag)
            else:
                result = "0.00-%.2fi" % (abs(self.imag))
        elif self.imag > 0:
            result = "%.2f+%.2fi" % (self.real, self.imag)
        else:
            result = "%.2f-%.2fi" % (self.real, abs(self.imag))
        return result
        

if __name__ == '__main__':
    c = map(float, input().split())
    d = map(float, input().split())
    x = Complex(*c)	# *c, *d are pointers I suppose. 
    y = Complex(*d)
    print(*map(str, [x+y, x-y, x*y, x/y, x.mod(), y.mod()]), sep='\n')


```
Notes- 

I found understanding both Classes and Complex Numbers tricky. 

https://pythongeeks.org/python-arguments/

Variable length arguments

These arguments are also used when we have a problem of number of arguments. To be specific, these arguments are used when we do not know number of arguments are needed to be passed to the function. These are also called arbitrary arguments.

In this case we use the the asterisk (*) before the parameter name in the definition of the function. For example,

Example of a function with variable length arguments:
def sum(*nos):
    total=0
    for i in nos:
        total=total+i
    print(total)
    
sum()
sum(-3,4,5)
sum(1,2,3,4,5)

Output:
0
6
15

https://www.w3schools.com/python/gloss_python_function_arbitrary_arguments.asp
https://www.geeksforgeeks.org/args-kwargs-python/


_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 
https://www.hackerrank.com/challenges/class-2-find-the-torsional-angle/problem

Discussion Answers-
https://www.hackerrank.com/challenges/class-2-find-the-torsional-angle/forum


```pycon
import math

class Points(object):
    def __init__(self, x, y, z):
        self.x= x
        self.y= y
        self.z= z
    def __sub__(self, no):
        return  Points((self.x-no.x),(self.y-no.y),(self.z-no.z))
    def dot(self, no):
        return (self.x*no.x)+(self.y*no.y)+(self.z*no.z)
    def cross(self, no):
        return Points((self.y*no.z-self.z*no.y),(self.z*no.x-self.x*no.z),(self.x*no.y-self.y*no.x))
    def absolute(self):
        return pow((self.x ** 2 + self.y ** 2 + self.z ** 2), 0.5)

if __name__ == '__main__':
    points = list()
    for i in range(4):
        a = list(map(float, input().split()))
        points.append(a)

    a, b, c, d = Points(*points[0]), Points(*points[1]), Points(*points[2]), Points(*points[3])
    x = (b - a).cross(c - b)
    y = (c - b).cross(d - c)
    angle = math.acos(x.dot(y) / (x.absolute() * y.absolute()))

    print("%.2f" % math.degrees(angle))
```
Notes- 

_____________

###### Question- find-a-string
https://www.hackerrank.com/challenges/find-a-string/problem

Discussion Answers-
https://www.hackerrank.com/challenges/find-a-string/forum


```pycon
# First attempt.
string= input()
sub_string= input()
start= 0
count= 0
for i in range(in):
	start= in.find(sub_string, start)
	if(start == -1):
    		print("Substring doesn't exist in the string")
	else:
    		print("The substring is found on position : ",start)
		count+= 1 

# Second attempt.
def count_substring(string, sub_string):
    start= 0
    count= 0
    
    for i in range(len(string)):
        start= string.find(sub_string, start)
        if(start == -1):
            # print("Substring doesn't exist in the string")
        else:
            # print("The substring is found on position : ",start)
            start+= 1
            count+= 1 
    return count

if __name__ == '__main__':
    string = input().strip()
    sub_string = input().strip()
    
    count = count_substring(string, sub_string)
    print(count)


# Submitted answer- Successful. 
def count_substring(string, sub_string):
    start, count= 0, 0    
    for i in range(len(string)):
        start= string.find(sub_string, start)
        if(start != -1):
            start+= 1
            count+= 1 
    return count

if __name__ == '__main__':
    string = input().strip()
    sub_string = input().strip()
    
    count = count_substring(string, sub_string)
    print(count)

# Discussion answer
string, substring = (input().strip(), input().strip())
print(sum([ 1 for i in range(len(string)-len(substring)+1) if string[i:i+len(substring)] == substring]))

# Discussion answer 2
def count_substring(s, sub):
    return [s[i:i+len(sub)] for i in range(len(s))].count(sub)

# Discussion answer 3
import re
def count_substring(string, sub_string):
    return len(re.findall("(?=" + sub_string + ")", string))

```
Notes- 

_____________

###### Question- python-time-delta
https://www.hackerrank.com/challenges/python-time-delta/problem

Discussion Answers-
https://www.hackerrank.com/challenges/python-time-delta/forum


```pycon
# Discussion Answer

#!/bin/python3

import math
import os
import random
import re
import sys
import datetime

# Complete the time_delta function below.
def time_delta(t1, t2):
    first = datetime.datetime.strptime(t1,'%a %d %b %Y %H:%M:%S %z')
    second = datetime.datetime.strptime(t2,'%a %d %b %Y %H:%M:%S %z')
    return str(abs(int((first-second).total_seconds())))
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    t = int(input())

    for t_itr in range(t):
        t1 = input()

        t2 = input()

        delta = time_delta(t1, t2)

        fptr.write(delta + '\n')

    fptr.close()

```
Notes- 


_____________

###### Question- words-score
https://www.hackerrank.com/challenges/words-score/problem

Discussion Answers-
https://www.hackerrank.com/challenges/words-score/forum


```pycon

# My answer- Just moved line 'num_vowels= 0' out of the for loop.
# 8/12 test cases failed :(
def is_vowel(letter):
    return letter in ['a', 'e', 'i', 'o', 'u', 'y']

def score_words(words):
    score = 0
    num_vowels = 0
    for word in words:
        for letter in word:
            if is_vowel(letter):
                num_vowels += 1
        if num_vowels % 2 == 0:
            score += 2
        else:
            ++score
    return score


n = int(input())
words = input().split()
print(score_words(words))

#Custom input
# 5
# vuv tpikawrurtmtcrs ajhgby tbnvycfnc bdczzgqygrpvoploooab

# 3
# programming is awesome
# Ans- 4
# MyAns- 5

# Second attempt- Congratulations- Passed all tests.
def is_vowel(letter):
    return letter in ['a', 'e', 'i', 'o', 'u', 'y']

def score_words(words):
    score = 0
    for word in words:
        num_vowels = 0
        for letter in word:
            if is_vowel(letter):
                num_vowels += 1
                #print ("letter= ", letter, num_vowels)
        if num_vowels % 2 == 0:
            score += 2
            #print ("even", score)
        else:
            score += 1
            #print ("odd", score)
    return score

n = int(input())
words = input().split()
print(score_words(words))


```
Notes- I think the line ++score doesn't work in Python. 


_____________

###### Question- python-lists
https://www.hackerrank.com/challenges/python-lists/problem

Discussion Answers-
https://www.hackerrank.com/challenges/python-lists/forum


```pycon
# Discussion Answers
n = int(input())
l = []
for _ in range(n):
    s = input().split()
    cmd = s[0]
    args = s[1:]
    if cmd !="print":
        cmd += "("+ ",".join(args) +")"
        eval("l."+cmd)
    else:
        print (l)

# Alternative Discussion Answer
n = int(input())
operations = [input().strip() for _ in range(n)]

list_ = []

commands = {
    'insert': lambda idx, ele: list_.insert(int(idx), int(ele)),
    'print': lambda: print(list_),
    'remove': lambda ele: list_.remove(int(ele)),
    'append': lambda ele: list_.append(int(ele)),
    'sort': lambda: list_.sort(),
    'pop': lambda: list_.pop(),
    'reverse': lambda: list_.reverse(),
}

for operation in operations:
    name, args = [i.strip() for i in (operation + ' ').split(' ', maxsplit=1)]
    command = commands.get(name)
    command(*args.split())

# Using Getattr
if __name__ == '__main__':
    N = int(raw_input())
    my_list=[]
    for x in range(N):
        args= raw_input().strip().split()
        args[1:]=map(int,args[1:])
        try:
            getattr(my_list,args[0])(*args[1:])
        except AttributeError:
            print my_list

# It's possible there is also a good solution using exec rather # than eval
if __name__ == '__main__':
    N = int(input())
    li = list()
    for dummy in range(N):
        command = input().split()
        try:
            getattr(li, command[0])(*(map(int, command[1:])))
        except AttributeError:
            exec('{}({})'.format(command[0], 'li'))


```
Notes- 

_____________

###### Question- zipped
https://www.hackerrank.com/challenges/zipped/problem

Discussion Answers-
https://www.hackerrank.com/challenges/zipped/forum


```pycon
# First attempt
N, X= input().split()

print (N, X)
scores= []
row_int= []
sum= 0
for i in range(int(N)):
    row= input().split()
    for j in row:
        sum = sum + float(j)
    print (sum/int(X))


# Discussion Answers
scores = []
n, x = map(int, input().split())
for i in range(x):
    scores.append(list(map(float, input().split())))
print(*[sum(student)/len(student) for student in zip(*scores)],sep='\n')

# Or
a,y = map(int, input().split())
scores = [map(float, input().split()) for _ in range(y)]

[print(sum(student)/y) for student in zip(*scores)]



```
Notes- 

_____________

###### Question- input
https://www.hackerrank.com/challenges/input/problem

Discussion Answers-
No Discsussion Tab


```pycon
x, k= map(int, input().split())
equation= input()
print (eval(equation)== k)
```
Notes- 

_____________

###### Question- 
https://www.hackerrank.com/challenges/polar-coordinates/problem

Discussion Answers-
https://www.hackerrank.com/challenges/polar-coordinates/forum


```pycon
#My Answer-success
import cmath
z= complex(input())
print (abs(z))
print(cmath.phase(z))

# Discussion Answer
import cmath
print(*cmath.polar(complex(input())), sep='\n')

#Also
x,y = map(float,re.findall('[+-]?\d+\.?\d*',raw_input().strip()))

#Also
from cmath import phase
print((lambda x: '%.3f\n%.3f' % (abs(x), phase(x)))(complex(input())))


```
Notes- 

_____________

###### Question- find-angle
https://www.hackerrank.com/challenges/find-angle/problem

Discussion Answers-
https://www.hackerrank.com/challenges/find-angle/forum

```pycon
from math import *

ab = float(input())
bc = float(input())
print(str(int(round(degrees(atan(ab/bc)),0)))+ '\u00B0')

```
Notes- There seems to be some issues with this question. I didn't spend a lot of time on it- but I don't think that they can use the equation- unless angle MBC = ACB (equation used to calculate angle ACB- ACB angle= arctan(opp- AB/adj- BC))

_____________

###### Question- xml-1-find-the-score
https://www.hackerrank.com/challenges/xml-1-find-the-score/problem

Discussion Answers-
https://www.hackerrank.com/challenges/xml-1-find-the-score/forum


```pycon
import sys
import xml.etree.ElementTree as etree

def get_attr_number(node):
    return str(etree.tostring(node)).count("=")

if __name__ == '__main__':
    sys.stdin.readline()
    xml = sys.stdin.read()
    tree = etree.ElementTree(etree.fromstring(xml))
    root = tree.getroot()
    print(get_attr_number(root))

```
Notes- 
_____________

###### Question- XML2 - Find the Maximum Depth
https://www.hackerrank.com/challenges/xml2-find-the-maximum-depth/problem

Discussion Answers-
https://www.hackerrank.com/challenges/xml2-find-the-maximum-depth/forum

```pycon

#Discussion Answer
import xml.etree.ElementTree as etree

maxdepth = 0
def depth(elem, level):
    global maxdepth
    # your code goes here
    if (level == maxdepth):
        maxdepth += 1
    for child in elem:
        depth(child, level + 1)        

if __name__ == '__main__':
    n = int(input())
    xml = ""
    for i in range(n):
        xml =  xml + input() + "\n"
    tree = etree.ElementTree(etree.fromstring(xml))
    depth(tree.getroot(), -1)
    print(maxdepth)


```
Notes- 

_____________

###### Question- swap-case
https://www.hackerrank.com/challenges/swap-case/problem

Discussion Answers-
https://www.hackerrank.com/challenges/swap-case/forum


```pycon
def swap_case(s):
    res= ""
    for i in range(len(s)):
        res= res+ s[i].swapcase()        
    return res

if __name__ == '__main__':
    s = input()
    result = swap_case(s)
    print(result)

# Alternative Answer
def swap_case(s):
    result = ""
    for letter in s:
        if letter == letter.upper():
            result += letter.lower()
        else:
            result += letter.upper()
    return result

# Alternative Answer 2

def swap_case(s):
    a = list(s)
    b = []
    for i in a:
        if i.islower():
             b.append(i.upper())
        else:
            b.append(i.lower())
    return("".join(b))

print(swap_case(input()))

# Alternative Answer 3

return "".join(list(map(lambda x : x.lower() if x.isupper() else x.upper(), list(s)))) 


```
Notes- 


_____________

###### Question- python-string-split-and-join
https://www.hackerrank.com/challenges/python-string-split-and-join/problem

Discussion Answers-
https://www.hackerrank.com/challenges/python-string-split-and-join/forum


```pycon

def split_and_join(line):
    # write your code here
    line = line.split(" ")
    line = "-".join(line)
    return line

if __name__ == '__main__':
    line = input()
    result = split_and_join(line)
    print(result)

```
Notes- 


_____________

###### Question- whats-your-name
https://www.hackerrank.com/challenges/whats-your-name/problem

Discussion Answers-
https://www.hackerrank.com/challenges/whats-your-name/forum

```pycon
#
# Complete the 'print_full_name' function below.
#
# The function is expected to return a STRING.
# The function accepts following parameters:
#  1. STRING first
#  2. STRING last
#

def print_full_name(first, last):
    # Write your code here
    print ("Hello {0} {1}! You just delved into python.".format(first, last))

if __name__ == '__main__':
    first_name = input()
    last_name = input()
    print_full_name(first_name, last_name)
```
Notes- 

_____________

###### Question- python-mutations
https://www.hackerrank.com/challenges/python-mutations/problem

Discussion Answers-
https://www.hackerrank.com/challenges/python-mutations/forum


```pycon
def mutate_string(string, position, character):
    string = string[:position] + character + string[(position+1):]
    return string

if __name__ == '__main__':
    s = input()
    i, c = input().split()
    s_new = mutate_string(s, int(i), c)
    print(s_new)
```
Notes- 

_____________

###### Question- validate-list-of-email-address-with-filter
https://www.hackerrank.com/challenges/validate-list-of-email-address-with-filter/problem

Discussion Answers-
https://www.hackerrank.com/challenges/validate-list-of-email-address-with-filter/forum


```pycon
def fun(s):

    # return True if s is a valid email, else return False
    try:
        username, url = s.split("@")
        website, extension = url.split(".")
        if any([username=='',website=='',url=='']): return False
    except ValueError:
        return  False
                
    cond1 = all(map(lambda x : 
    x.isdigit() or 
    x.isupper() or 
    x.islower() or 
    x == '-' or x=='_', 
    username))
        
    cond2 = all(map(lambda x : 
    x.isdigit() or 
    x.isupper() or 
     x.islower(), 
    website))
        
    cond3 = 0< len(extension) < 4
    
    return all([cond1,cond2,cond3])
    
def filter_mail(emails):
    return list(filter(fun, emails))

if __name__ == '__main__':
    n = int(input())
    emails = []
    for _ in range(n):
        emails.append(input())

filtered_emails = filter_mail(emails)
filtered_emails.sort()
print(filtered_emails)

```
Notes- 

_____________

###### Question- incorrect-regex
https://www.hackerrank.com/challenges/incorrect-regex/problem

Discussion Answers-
https://www.hackerrank.com/challenges/incorrect-regex/forum


```pycon
import re
for _ in range(int(input())):
    ans = True
    try:
        reg = re.compile(input())
    except re.error:
        ans = False
    print(ans)

```
Notes- 

_____________

###### Question- itertools-product
https://www.hackerrank.com/challenges/itertools-product/problem

Discussion Answers-
https://www.hackerrank.com/challenges/itertools-product/forum


```pycon
#First Step
a1, a2= input().split()
b1, b2= input().split()
print (a1, a2)
print (b1, b2)
# 
a1, a2= input().split()
b1, b2= input().split()
print ("(",a1,",",b1,")",  "(", a1, ",", b2, ")",  "(", a2, ",", b1, ")", "(", a2, ",", b2, ")" )
# The print command is adding spaces to the output which isn't validating-> Supposed to use itertools to do the problem. 
# Discussion Answer
from itertools import product

A = list(map(int, input().split()))
B = list(map(int, input().split()))
p = product(A,B)
print(*p)


```
Notes- Not sure about the *p. 

_____________

###### Question- itertools-permutations
https://www.hackerrank.com/challenges/itertools-permutations/problem

Discussion Answers-
https://www.hackerrank.com/challenges/itertools-permutations/forum


```pycon
#First attempt
from itertools import permutations
a, b= input().split()
out= sorted(list(permutations(a,int(b))))
print (out)

#Second attempt with help
from itertools import permutations
a, b= input().split()
out= sorted(list(permutations(a,int(b))))
for i in out:
    print(*i,sep='')

```
Notes- 
_____________

###### Question- itertools-combinations
https://www.hackerrank.com/challenges/itertools-combinations/problem

Discussion Answers-
https://www.hackerrank.com/challenges/itertools-combinations/forum


```pycon
# Just the previous question with combinations substituted for permutations- but it's not quite.

# First attempt
from itertools import combinations
a, b= input().split()
out= []
out= sorted(list(combinations(a,int(b))))
for i in out:
    print(*i,sep='')

#Second attempt
from itertools import combinations
a, b= input().split()
out= []
for j in range(int(b)+1):
    out= out + sorted(list(combinations(a,int(j)))) # The + may be an issue here. 
for i in out:
    if not i== []:  # There was a null value in the answer this is an attempt to remove it. 
        print(*i,sep='')

# Discussion answer
from itertools import combinations

if __name__=="__main__":
    cmds = input().split()
    word ="".join( sorted(cmds[0] ))
    size = int(cmds[1])
    for _i in range(size):
        [print ("".join(i)) for i in list(combinations(word, _i+1))  ]


```
Notes- 

_____________

###### Question- combinations_with_replacement
https://www.hackerrank.com/challenges/itertools-combinations-with-replacement/problem

Discussion Answers-
https://www.hackerrank.com/challenges/itertools-combinations-with-replacement/forum


```pycon

# First attempt
from itertools import combinations_with_replacement
a, b= input().split()
out= sorted(list(combinations_with_replacement(a,int(b))))
for i in out:
    print(*i,sep='')

#Discussion answer
from itertools import combinations_with_replacement

s, k = input().split()
for t in sorted(combinations_with_replacement(sorted(s), int(k))):
    print("".join(t))


```
Notes- 


_____________

###### Question- compress-the-string
https://www.hackerrank.com/challenges/compress-the-string/problem

Discussion Answers-
https://www.hackerrank.com/challenges/compress-the-string/forum


```pycon

#Discussion answers
from itertools import groupby
for key, count in groupby(*input().split()):
    print("({}, {})".format(len(list(count)),key),end=" ")

#Interesting
from itertools import groupby
print(*[(len(list(g)),int(k))for k,g in groupby(input())])

#My answer
from itertools import groupby
for key, count in groupby(input()):
    print("({}, {})".format(len(list(count)),key),end=" ")  #?

```
Notes- 
https://docs.python.org/3.8/library/itertools.html#itertools.groupby

_____________

###### Question- iterables-and-iterators
https://www.hackerrank.com/challenges/iterables-and-iterators/problem

Discussion Answers-
https://www.hackerrank.com/challenges/iterables-and-iterators/forum


```pycon
#Discussion answer
from itertools import combinations 
n = int(input())
s = input().split()
k = int(input())
com = list(combinations(s,k))
print(len([x for x in com if "a" in x])/len(com))

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 
_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 


_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 


_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 

_____________

###### Question- 


Discussion Answers-



```pycon

```
Notes- 
