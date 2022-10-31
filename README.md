# Zenpass

[![PyPI](https://img.shields.io/pypi/v/zenpass)](https://pypi.python.org/pypi/zenpass)
[![PyPI - License](https://img.shields.io/pypi/l/zenpass)](https://github.com/codesrg/zenpass/blob/main/LICENSE)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/zenpass?color=red)](https://pypi.python.org/pypi/zenpass)

To generate random and strong passwords.

## Installation

`pip install -U zenpass`

## Usage

```
usage: zenpass [options]

optional arguments:
  -h, --help         show this help message and exit
  -v, --version      show version number and exit.

to customize Password:
  -l , --length      to set length to the password
  -n , --ignore      to ignore unwanted characters to the password
  -i , --include     to include characters to the password
  -o , --only        to create password only using wanted characters
  -s , --separator   the separator character
  -c , --seplen      the length of characters between separator
  --repeat           to repeat the characters in the password (default : False)
  --separation       to separate password characters using separator (default : False)
```

###
To generate a random password and print it on the screen.
```
> zenpass
kj(ot--4mJ1aeJ
```
###

To set the password length, Default password length is `8-16`.

```
> zenpass -l 10
Q3m/vro|uR
```
###

Whether the characters in passwords repeat or not,
Default value of `repeat` is `False`.
```
> zenpass -r
96Ndl;1D>jQu4Z2
```
###

To include, ignore or use only `'alphabets'`, `'numbers'`, `'uppercase'`, `'lowercase'`, `'symbols'` and `random characters` in generating password.
###

To ignore `numbers` in passwords. 

```
> zenpass -n numbers
uyMXP‘$!ZSCYqzj
```
###
To ignore characters `a,b,c,d,e`
```
> zenpass -n abcde
~}t"R‘jF'ksG8~E
```
###
To create a password only using `special characters`.

```
> zenpass -o symbols -l 15
?)".=-_^[_‘~{.)
```
###
To include `a,b,c,d,e` characters in a password.
```
> zenpass -o numbers -i abcde -l 15
78713d1e3d926a3
```
###
To separate characters in a password using separator.
```
> zenpass -o uppercase --separation -l 16
YNQC-RKBF-DMAT-UVIP
```
###
To separate characters in a password using separator `_` with `5` characters between each separator.
```
> zenpass -o uppercase --separation -l 15 -s _ -c 5 
YNQCR_KBFDM_ATUVI
```

## Issues:

If you encounter any problems, please file an [issue](https://github.com/codesrg/zenpass/issues) along with a detailed description.