
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



