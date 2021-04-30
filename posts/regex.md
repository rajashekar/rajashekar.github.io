<!--
.. title: Regex
.. slug: regex
.. date: 2020-06-17 05:41:20 UTC-07:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

<img src="/images/regular_expressions.png" style="display: block;margin-left: auto;margin-right: auto;">
---
<!-- TEASER_END -->

Below is overview on Regex standards
<img src="/images/regex_standards.png" width="50%" style="display: block;margin-left: auto;margin-right: auto;"/>

Below are few commands and examples of Regular expressions.
1. Dot - `.` any character except newline 

2. `\w` `\d` `\s` - word, digit, whitespace
```
Example:
substitution 
a. %s/\(\w\+\)/"\1"/g

before:
test test test

after:
"test" "test" "test"

b. %s/\(\d\+\)/"\1"/g
before:
test test test 
123 123 1234 123456

after:
test test test 
"123" "123" "1234" "123456"
```
3. `\W` `\D` `\S` not word, digit, whitespace

4. `[abc]` any of a, b, or c

5. `[^abc]` not a, b, or c

6. `[a-g]` character between a & g

7. `^abc$` start / end of the string

8. `\t` `\n` `\r` tab, linefeed, carriage return

9. `a*`  0 or more

10. `a+`  1 or more

11. `a?` 0 or 1

12. `a{5}`  exactly 5

13. `a{2,}` 2 or more

14. `a{3,5}` - matches 3, 4, 5

15. `&` Back reference without grouping 
```
:%s/test/"&"/g

before:
test | test | test | test | test | test 

after:
"test" | "test" | "test" | "test" | "test" | "test"
```
16. Grouping - `(abc)`
`\1` backreference
```
Example - 
^/sams/cart/(cart.jsp)/test/\1$

matches - 
/sams/cart/cart.jsp/test/cart.jsp

Not matches - 
/sams/cart/test/cart.jsp
/sams/cart/cart.jsp
/sams/cart/cart.jsp/test
```

17. non-capturing group - `(?:abc)`
```
Example - 
^/sams/cart/(?:cart.jsp)/(test)/\1$

matches - 
/sams/cart/cart.jsp/test/test

not matches - 
/sams/cart/test/cart.jsp
/sams/cart/cart.jsp
/sams/cart/cart.jsp/test
```

18. Negative lookahead - `(?!abc)`
Example - 
```
^/sams/cart/(?!cart.jsp).*jsp$

matches - 
/sams/cart/test/cart.jsp
/sams/cart/cartService.jsp
/sams/cart/saveForLater.jsp

Not matches - 
/sams/cart/cart.jsp?xid=123&redirectURL=test.jsp
```

19. Postive lookahead - `(?=abc)`
Example - 
```
^/sams/cart/(?=cart.jsp).*jsp$

matches - 
/sams/cart/cart.jsp?xid=123&redirectURL=test.jsp

not matches - 
/sams/cart/test/cart.jsp
/sams/cart/cartService.jsp
/sams/cart/saveForLater.jsp
```

20. Named Capturing Group - `(?P<abc>.*) or {?<abc>.*)`
```
Example: 

([^|]+\|){3}(?P<xyz>[^|]+)

test1 | test2 | test3 | test4 | test5 | test6 

xyz is test4
```

### Playgrounds
https://regexr.com/37kj6 <br>
https://www.regexpal.com/ <br>
https://regex101.com/r/I4moyv/1 <br>

For java - https://www.freeformatter.com/java-regex-tester.html#ad-output