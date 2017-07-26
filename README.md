# Pyliners

**Tweets of [@pyliners](https://twitter.com/pyliners)**

Neat little Python recipes in under 140 characters

---

## Table of Contents

- [URL encode a string in Python](#url-encode-a-string-in-python)
- [Diff two directories](#diff-two-directories)
- [Get ASN details for an IP address](#get-asn-details-for-an-ip-address)
- [Covert a string to ROT13](#covert-a-string-to-rot13)
- [Display list of all the users on Unix-like systems](#display-list-of-all-the-users-on-unix-like-systems)
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

### URL encode a string in Python

```python
python -c "import urllib; print urllib.quote_plus('string_of_characters_like_these:$#@=?%^Q^$')"
```

### Diff two directories

- Diff two directories
- Prints the contents that are unique to each directory

```python
python -m filecmp dir1 dir2
```

### Get ASN details for an IP address

- Handy during information gathering in a pentest

```python
echo 8.8.8.8 | python -c "import urllib,json,sys;print json.load(urllib.urlopen('https://api.iptoasn.com/v1/as/ip/'+sys.stdin.read()))['as_number']"
```

```bash
curl -s http://ip-api.com/json/8.8.8.8  | python -c 'import sys, json; print json.load(sys.stdin)["as"]'
```

### Covert a string to ROT13

- ROT13 is a substitution cipher, it's fairly common to see ROT13 strings as part of CTF challenges

```python
python -m encodings.rot_13 <<< "Sample string"
```


### Display list of all the users on Unix-like systems

- Requires read access to `/etc/passwd` file

```python
python -c "print '\n'.join(line.split(':',1)[0] for line in open('/etc/passwd'))"
```

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
python -m base64 <<< 'apple'
```

### Print a calender

- Prints a calender

```
python -m calendar
```


### Print the platform details

- Prints the underlying platform details
- `platform` module is OS agnostic.

```python
python -m platform
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