# Pyliners

**Tweets of [@pyliners](https://twitter.com/pyliners)**

Neat little Python recipes in under 140 characters

---

## Table of Contents

- [Decode base64](#decode-base64)
- [Encode a string to base64](#encode-a-string-to-base64)
- [Print a calender](#print-a-calender)
- [Print the platform details](#print-the-platform-details)
- [Minimal HTTP server Python3.x](#minimal-http-server-python3x)
- [Minimal HTTP server Python2.x](#minimal-http-server-python2x)
- [Print zen of Python](#print-the-zen-of-python)
- [Import antigravity](#import-antigravity)
- [Print "Hello, world!"](#print-hello-world)

---

### Decode base64

- Decode base64 encoded string
- Comes handy during pentests/CTFs

```python
python -m base64 -d <<< "dGhpcyBpcyBlbmNvZGVkCg=="
```
### Encode a string to base64 

- Encode a string to base64
- Comes handy during pentests/CTFs

```python
$ python -m base64 <<< 'apple'
```

### Print a calender

- Prints a calender

```
$ python -m calendar
```


### Print the platform details

- Prints the underlying platform details
- `platform` module is OS agnostic.

```python
$ python -m platform
```

### Minimal HTTP server Python3.x

- Minimal HTTP server in Python 3.X 
- Comes handy when transfer files(esp during pen testing)

```python
python -m http.server 8000
```

### Minimal HTTP server Python2.x

- Minimal HTTP server that supports GET and HEAD request handlers
- Comes handy when transfer files(esp during pen testing)

```python
python -m SimpleHTTPServer 8000 
```


### Print the zen of Python

- [The Zen of Python](https://en.wikipedia.org/wiki/Zen_of_Python) is a collection of software principles that influences the design of Python Programming Language
- Fowiing snippet prints the zen of python

```python
python -m this
```

### Import antigravity

- The antigravity module, opens the [XKCD comic mentioning Python](https://xkcd.com/353/) in a web browser

```python
python -c "import antigravity"
```

### Print hello world

- This snippet will simply print the "Hello, world!" string(Python2.x syntax)
- In Python3, print is a function not a keyword

```python
print "Hello, world!"
```