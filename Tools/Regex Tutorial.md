### Regex Tutorial

* **a, X, 9,** < -- ordinary characters just match themselves exactly. The meta-characters which do not match themselves because they have special meanings are: `. ^ $ * + ? { [ ] \ | ( )` (details below)
* **.** (a period) -- matches any single character except newline '\n'
* **\w** -- (lowercase w) matches a "word" character: a letter or digit or underbar [a-zA-Z0-9_]. Note that although "word" is the mnemonic for this, it only matches a single word char, not a whole word. \W (upper case W) matches any non-word character.
* **\b** -- boundary between word and non-word
* **\s** -- (lowercase s) matches a single whitespace character -- space, newline, return, tab, form [ \n\r\t\f]. \S (upper case S) matches any non-whitespace character.
* **\t, \n, \r** -- tab, newline, return
* **\d** -- decimal digit [0-9] (some older regex utilities do not support but \d, but they all support \w and \s)
* **^ = start, $ = end** -- match the start or end of the string
* ** \ ** -- inhibit the "specialness" of a character. So, for example, use \. to match a period or \\ to match a slash. If you are unsure if a character has special meaning, such as '@', you can put a slash in front of it, \@, to make sure it is treated just as a character.


### Escape sequences

There are some special characters starting with backslash \ which are known as the escape or control sequences. They do not have corresponding symbols and cannot be found on a keyboard. To represent such characters we use a pair of regular symbols. In a program, this pair will be considered as exactly one character with the appropriate code.

* '\n' is the newline character;
* '\t' is the tab character;
* '\r' is the carriage return character;
* '\\' is the backslash character itself;
* '\'' is the single quote mark;
* '\"' is the double quote mark.