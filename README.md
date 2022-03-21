# semgrep-rules
[![](https://img.shields.io/github/stars/0xdea/semgrep-rules.svg?color=yellow)](https://github.com/0xdea/semgrep-rules)
[![](https://img.shields.io/github/forks/0xdea/semgrep-rules.svg?color=green)](https://github.com/0xdea/semgrep-rules)
[![](https://img.shields.io/github/watchers/0xdea/semgrep-rules.svg?color=red)](https://github.com/0xdea/semgrep-rules)
[![](https://img.shields.io/badge/license-MIT%20License-red.svg?color=lightgray)](https://opensource.org/licenses/MIT) 
[![](https://img.shields.io/badge/twitter-%400xdea-blue.svg)](https://twitter.com/0xdea)

> "Humans are more suited to recognize food than to keep large graphs in their head." 
> 
> -- @halvarflake

A collection of my Semgrep rules to facilitate vulnerability research.

See also: https://semgrep.dev/r

## C/C++

### buffer overflows
* [**insecure-api-gets**](https://github.com/0xdea/semgrep-rules/blob/main/c/insecure-api-gets.yaml). Use of the insecure API function gets().
* [**insecure-api-strcpy-stpcpy-strcat**](https://github.com/0xdea/semgrep-rules/blob/main/c/insecure-api-strcpy-stpcpy-strcat.yaml). Use of the potentially insecure API functions strcpy(), stpcpy(), strcat().
* [**unterminated-string-strncpy-stpncpy**](https://github.com/0xdea/semgrep-rules/blob/main/c/unterminated-string-strncpy-stpncpy.yaml). Lack of explicit null-termination after strncpy() and stpncpy().
* [**unsafe-ret-strlcpy-strlcat**](https://github.com/0xdea/semgrep-rules/blob/main/c/unsafe-ret-strlcpy-strlcat.yaml). Potentially unsafe use of the return value of strlcpy() and strlcat().
* [**unsafe-ret-snprintf-vsnprintf**](https://github.com/0xdea/semgrep-rules/blob/main/c/unsafe-ret-snprintf-vsnprintf.yaml). Potentially unsafe use of the return value of snprintf() and vsnprintf().

### format strings
* [**format-string-bugs**](https://github.com/0xdea/semgrep-rules/blob/main/c/format-string-bugs.yaml). Potential format string bugs.

### integer overflows
* [**integer-truncation**](https://github.com/0xdea/semgrep-rules/blob/main/c/integer-truncation.yaml). Potential integer truncation errors.
* [**unsafe-strlen**](https://github.com/0xdea/semgrep-rules/blob/main/c/unsafe-strlen.yaml). Casting the return value of strlen() to short might be dangerous.

### privilege management
* [**unchecked-ret-setuid-seteuid**](https://github.com/0xdea/semgrep-rules/blob/main/c/unchecked-ret-setuid-seteuid.yaml). Unchecked return code of setuid() and seteuid() functions.

### miscellaneous
* [**interesting-api-calls**](https://github.com/0xdea/semgrep-rules/blob/main/c/interesting-api-calls.yaml). Calls to interesting and potentially insecure API functions.
