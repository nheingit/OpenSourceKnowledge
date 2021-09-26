Python has an `re` module that you can import to implement regex searches

it has 3 key functions that I use:

`re.match`, `re.search`, `re.sub`

match and search are almost identical, there is one key difference however:
 [`re.match()`](https://docs.python.org/3/library/re.html#re.match "re.match") checks for a match only at the beginning of the string, while [`re.search()`](https://docs.python.org/3/library/re.html#re.search "re.search") checks for a match anywhere in the string
 
 ```python
 >>> re.match("c", "abcdef")    # No match
>>> re.search("c", "abcdef")   # Match
 ```

[`re.sub()`](https://docs.python.org/3/library/re.html#re.sub)
will replace whatever the matched instance is with the replacement arg.
```python
result = re.sub('abc',  '',    input)           # Delete pattern abc
result = re.sub('abc',  'def', input)           # Replace pattern abc -> def
result = re.sub(r'\s+', ' ',   input)           # Eliminate duplicate whitespaces using wildcards
result = re.sub('abc(def)ghi', r'\1', input)    # Replace a string with a part of itself
```