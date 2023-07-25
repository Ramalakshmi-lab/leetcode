how to remove special chracter from some input string s1="hi hello. how, r u." to get output as "hi hello how r u" in python

method1:
import re

s1 = "hi hello. how, r u."
cleaned_s1 = re.sub(r'[^\w\s]', '', s1)

print(cleaned_s1)

method2:
s1 = "hi hello. how, r u."
cleaned_s1 = ''.join(char for char in s1 if char.isalnum() or char.isspace())

print(cleaned_s1)
