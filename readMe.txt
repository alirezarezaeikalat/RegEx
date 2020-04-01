1. regex is always has question. [ATTENTION]

2. use regex101.com for checking the regex templates.

3. regex always are between / /

4. for example /ninja/ finds ninja in the string in a case sensitive way

5. /ninja/g finds all the ninja in the string, not just the first one.
  g is a flag and stands for global.

6. /ninja/gi finds all the ninja in the insensitive format.
  i stands for insensitive.

7. how to match ninja and ginja by using character set.
  /[ng]inja/g this finds all the ginja and ninja in the string.
  remember [] only occupy one space in the regular expression

8. /[^p]00/g this match everything like u000 or z000 ... except
  p00

9. Range:
    /[a-z]inja/g  accept and fins all the chars at the first position, for
    example ninja, binja, ainja ...
    /[a-zA-Z]inja/g finds all the char in a insensitive format.
    /[0-9]inja/g

10. Repeating characters:
    /[0-9]+/g : match if at least one number in the string
    /[0-9]{11}/g : match eleven times 
    /[a-z]{5,8}/g : to match word with 5 to 8 letters long
    /[0-9] {5, }/g : find any match with at least with 5 number

11. Metacharacters:

    \d match any digit characters (same as [0-9])
    \w match any word characters (a-z, A-Z, 0-9 and _s)
    \s match any whitespace characters (spaces, tabs etc)
    \t match tab character only

12. The special characters after one character:

    + The one or more quantifier
    ? zero or one quantifier
    * zero or more quantifier
    \ the escape character (\* means * in the string)
    [] The character set
    [^] The negate symbol in a character set
    . Any character (except the new line character )

13. alternate character:  |
to match pyre and tyre   (p|t)yre

14. Starting(^) and Ending($) pattern:
    /^[a-z]{5}$/i  it means the five letter word must be at the 
    first and end of the word

15. we can make regular expressions in two ways:

    a. var reg = /a-z/g;
    b. var reg2 = new RegEx(/[a-z]/, "g");