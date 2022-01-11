---
title: "Regular Expression 2 syntax"
ms.author: comanea
author: dan-wesley
manager: seanlyn
ms.date: 01/11/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Regular Expression 2 syntax"
---

# Regular Expression 2 (re2.h) syntax

Regular expressions are a notation for describing sets of character strings. When a string is in the set described by a regular expression, we often say that the regular expression matches the string.

The simplest regular expression is a single literal character. Except for the metacharacters like `\*+?()|`, characters match themselves. To match a metacharacter, escape it with a backslash: `\+` matches a literal plus character.

Two regular expressions can be altered or concatenated to form a new regular expression: if *e<sub>1</sub>* matches _s_ and *e<sub>2</sub>* matches _t_, then *e<sub>1</sub>* | *e<sub>2</sub>* matches _s_ or _t_, and *e<sub>1</sub>* *e<sub>2</sub>*  matches _st_.

The metacharacters _`\`_ , _+_ , and _?_ are repetition operators: *e<sub>1</sub>* _`\`_ matches a sequence of zero or more (possibly different) strings, each of which match *e<sub>1</sub>*; *e<sub>1</sub>* _+_ matches one or more; *e<sub>1</sub>* _?_ matches zero or one.

The operator precedence, from weakest to strongest binding, is first alternation, then concatenation, and finally the repetition operators. Explicit parentheses can be used to force different meanings, as in arithmetic expressions. Some examples: _ab|cd_ is equivalent to _(ab)|(cd)_ ; _`ab\`_ is equivalent to _`a(b\)`_ .

The syntax described so far is most of the traditional Unix _egrep_ regular expression syntax. This subset suffices to describe all regular languages. A regular language is a set of strings that can be matched in a single pass through the text using only a fixed amount of memory. Newer regular expression facilities (notably Perl and those languages that have copied it) have added many new operators and escape sequences. These changes make the regular expressions more concise, and sometimes more cryptic, but not more powerful.

This page lists the regular expression syntax accepted by RE2.

It also lists some syntax accepted by PCRE, PERL, and VIM.

## Syntax tables

| Kinds of single-character expressions | Examples |
| --- | --- |
| any character, possibly including newline (s=true) | . |
| character class | [xyz] |
| negated character class | [^xyz] |
| Perl character class ([link](#user-content-perl)) | \d |
| negated Perl character class | \D |
| ASCII character class ([link](#user-content-ascii)) | [[:alpha:]] |
| negated ASCII character class | [[:^alpha:]] |
| Unicode character class (one-letter name) | \pN |
| Unicode character class | \p{Greek} |
| negated Unicode character class (one-letter name) | \PN |
| negated Unicode character class | \P{Greek} |

|&nbsp;| Composites |
| --- | --- |
| xy | x followed by y |
| x\|y | x or y (prefer x) |

|&nbsp;| Repetitions |
| --- | --- |
| x\* | zero or more x, prefer more |
| x+ | one or more x, prefer more |
| x? | zero or one x, prefer one |
| x{n,m} | n or n+1 or ... or m x, prefer more |
| x{n,} | n or more x, prefer more |
| x{n} | exactly n x |
| x\*? | zero or more x, prefer fewer |
| x+? | one or more x, prefer fewer |
| x?? | zero or one x, prefer zero |
| x{n,m}? | n or n+1 or ... or m x, prefer fewer |
| x{n,}? | n or more x, prefer fewer |
| x{n}? | exactly n x |
| x{} | (≡ x\*) (NOT SUPPORTED) VIM |
| x{-} | (≡ x\*?) (NOT SUPPORTED) VIM |
| x{-n} | (≡ x{n}?) (NOT SUPPORTED) VIM |
| x= | (≡ x?) (NOT SUPPORTED) VIM |

Implementation restriction: The counting forms x{n,m}, x{n,}, and x{n} reject forms that create a minimum or maximum repetition count above 1000. Unlimited repetitions are not subject to this restriction.

|&nbsp;| Possessive repetitions |
| --- | --- |
| x\*+ | zero or more x, possessive (NOT SUPPORTED) |
| x++ | one or more x, possessive (NOT SUPPORTED) |
| x?+ | zero or one x, possessive (NOT SUPPORTED) |
| x{n,m}+ | n or ... or m x, possessive (NOT SUPPORTED) |
| x{n,}+ | n or more x, possessive (NOT SUPPORTED) |
| x{n}+ | exactly n x, possessive (NOT SUPPORTED) |

|&nbsp;| Grouping |
| --- | --- |
| (re) | numbered capturing group (submatch) |
| (?P&lt;name&gt;re) | named &amp; numbered capturing group (submatch) |
| (?&lt;name&gt;re) | named &amp; numbered capturing group (submatch) (NOT SUPPORTED) |
| (?&#39;name&#39;re) | named &amp; numbered capturing group (submatch) (NOT SUPPORTED) |
| (?:re) | non-capturing group |
| (?flags) | set flags within current group; non-capturing |
| (?flags:re) | set flags during re; non-capturing |
| (?#text) | comment (NOT SUPPORTED) |
| (?\|x\|y\|z) | branch numbering reset (NOT SUPPORTED) |
| (?&gt;re) | possessive match of re (NOT SUPPORTED) |
| re@&gt; | possessive match of re (NOT SUPPORTED) VIM |
| %(re) | non-capturing group (NOT SUPPORTED) VIM |

|&nbsp;| Flags |
| --- | --- |
| i | case-insensitive (default false) |
| m | multi-line mode: ^ and $ match begin/end line in addition to begin/end text (default false) |
| s | let . match \n (default false) |
| U | ungreedy: swap meaning of x\* and x\*?, x+ and x+?, etc (default false) |

Flag syntax is xyz (set) or -xyz (clear) or xy-z (set xy, clear z).

|&nbsp;| Empty strings |
| --- | --- |
| ^ | at beginning of text or line (m=true) |
| $ | at end of text (like \z not \Z) or line (m=true) |
| \A | at beginning of text |
| \b | at ASCII word boundary (\w on one side and \W, \A, or \z on the other) |
| \B | not at ASCII word boundary |
| \g | at beginning of subtext being searched (NOT SUPPORTED) PCRE |
| \G | at end of last match (NOT SUPPORTED) PERL |
| \Z | at end of text, or before newline at end of text (NOT SUPPORTED) |
| \z | at end of text |
| (?=re) | before text matching re (NOT SUPPORTED) |
| (?!re) | before text not matching re (NOT SUPPORTED) |
| (?&lt;=re) | after text matching re (NOT SUPPORTED) |
| (?&lt;!re) | after text not matching re (NOT SUPPORTED) |
| re&amp; | before text matching re (NOT SUPPORTED) VIM |
| re@= | before text matching re (NOT SUPPORTED) VIM |
| re@! | before text not matching re (NOT SUPPORTED) VIM |
| re@&lt;= | after text matching re (NOT SUPPORTED) VIM |
| re@&lt;! | after text not matching re (NOT SUPPORTED) VIM |
| \zs | sets start of match (= \K) (NOT SUPPORTED) VIM |
| \ze | sets end of match (NOT SUPPORTED) VIM |
| \%^ | beginning of file (NOT SUPPORTED) VIM |
| \%$ | end of file (NOT SUPPORTED) VIM |
| \%V | on screen (NOT SUPPORTED) VIM |
| \%# | cursor position (NOT SUPPORTED) VIM |
| \%&#39;m | mark m position (NOT SUPPORTED) VIM |
| \%23l | in line 23 (NOT SUPPORTED) VIM |
| \%23c | in column 23 (NOT SUPPORTED) VIM |
| \%23v | in virtual column 23 (NOT SUPPORTED) VIM |

|&nbsp;| Escape sequences |
| --- | --- |
| \a | bell (≡ \007) |
| \f | form feed (≡ \014) |
| \t | horizontal tab (≡ \011) |
| \n | newline (≡ \012) |
| \r | carriage return (≡ \015) |
| \v | vertical tab character (≡ \013) |
| \* | literal \*, for any punctuation character \* |
| \123 | octal character code (up to three digits) |
| \x7F | hex character code (exactly two digits) |
| \x{10FFFF} | hex character code |
| \C | match a single byte even in UTF-8 mode |
| \Q...\E | literal text ... even if ... has punctuation |
| \1 | backreference (NOT SUPPORTED) |
| \b | backspace (NOT SUPPORTED) (use \010) |
| \cK | control char ^K (NOT SUPPORTED) (use \001 etc) |
| \e | escape (NOT SUPPORTED) (use \033) |
| \g1 | backreference (NOT SUPPORTED) |
| \g{1} | backreference (NOT SUPPORTED) |
| \g{+1} | backreference (NOT SUPPORTED) |
| \g{-1} | backreference (NOT SUPPORTED) |
| \g{name} | named backreference (NOT SUPPORTED) |
| \g&lt;name&gt; | subroutine call (NOT SUPPORTED) |
| \g&#39;name&#39; | subroutine call (NOT SUPPORTED) |
| \k&lt;name&gt; | named backreference (NOT SUPPORTED) |
| \k&#39;name&#39; | named backreference (NOT SUPPORTED) |
| \lX | lowercase X (NOT SUPPORTED) |
| \ux | uppercase x (NOT SUPPORTED) |
| \L...\E | lowercase text ... (NOT SUPPORTED) |
| \K | reset beginning of $0 (NOT SUPPORTED) |
| \N{name} | named Unicode character (NOT SUPPORTED) |
| \R | line break (NOT SUPPORTED) |
| \U...\E | upper case text ... (NOT SUPPORTED) |
| \X | extended Unicode sequence (NOT SUPPORTED) |
| \%d123 | decimal character 123 (NOT SUPPORTED) VIM |
| \%xFF | hex character FF (NOT SUPPORTED) VIM |
| \%o123 | octal character 123 (NOT SUPPORTED) VIM |
| \%u1234 | Unicode character 0x1234 (NOT SUPPORTED) VIM |
| \%U12345678 | Unicode character 0x12345678 (NOT SUPPORTED) VIM |

|&nbsp;| Character class elements |
| --- | --- |
| x | single character |
| A-Z | character range (inclusive) |
| \d | Perl character class |
| [:foo:] | ASCII character class foo |
| \p{Foo} | Unicode character class Foo |
| \pF | Unicode character class F (one-letter name) |

|&nbsp;| Named character classes as character class elements |
| --- | --- |
| [\d] | digits (≡ \d) |
| [^\d] | not digits (≡ \D) |
| [\D] | not digits (≡ \D) |
| [^\D] | not not digits (≡ \d) |
| [[:name:]] | named ASCII class inside character class (≡ [:name:]) |
| [^[:name:]] | named ASCII class inside negated character class (≡ [:^name:]) |
| [\p{Name}] | named Unicode property inside character class (≡ \p{Name}) |
| [^\p{Name}] | named Unicode property inside negated character class (≡ \P{Name}) |

| <a name="user-content-perl"></a> | Perl character classes (all ASCII-only) |
| --- | --- |
| \d | digits (≡ [0-9]) |
| \D | not digits (≡ [^0-9]) |
| \s | whitespace (≡ [\t\n\f\r]) |
| \S | not whitespace (≡ [^\t\n\f\r]) |
| \w | word characters (≡ [0-9A-Za-z\_]) |
| \W | not word characters (≡ [^0-9A-Za-z\_]) |
| \h | horizontal space (NOT SUPPORTED) |
| \H | not horizontal space (NOT SUPPORTED) |
| \v | vertical space (NOT SUPPORTED) |
| \V | not vertical space (NOT SUPPORTED) |

|<a name="user-content-ascii"></a>  | ASCII character classes |
| --- | --- |
| [[:alnum:]] | alphanumeric (≡ [0-9A-Za-z]) |
| [[:alpha:]] | alphabetic (≡ [A-Za-z]) |
| [[:ascii:]] | ASCII (≡ [\x00-\x7F]) |
| [[:blank:]] | blank (≡ [\t]) |
| [[:cntrl:]] | control (≡ [\x00-\x1F\x7F]) |
| [[:digit:]] | digits (≡ [0-9]) |
| [[:graph:]] | graphical (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`) |
| [[:lower:]] | lower case (≡ [a-z]) |
| [[:print:]] | printable (≡ [-~] ≡ [[:graph:]]) |
| [[:punct:]] | punctuation (≡ [!-/:-@[-`{-~]) |
| [[:space:]] | whitespace (≡ [\t\n\v\f\r]) |
| [[:upper:]] | upper case (≡ [A-Z]) |
| [[:word:]] | word characters (≡ [0-9A-Za-z\_]) |
| [[:xdigit:]] | hex digit (≡ [0-9A-Fa-f]) |

|&nbsp;| Unicode character class names--general category |
| --- | --- |
| C | other |
| Cc | control |
| Cf | format |
| Cn | unassigned code points (NOT SUPPORTED) |
| Co | private use |
| Cs | surrogate |
| L | letter |
| LC | cased letter (NOT SUPPORTED) |
| L&amp; | cased letter (NOT SUPPORTED) |
| Ll | lowercase letter |
| Lm | modifier letter |
| Lo | other letter |
| Lt | titlecase letter |
| Lu | uppercase letter |
| M | mark |
| Mc | spacing mark |
| Me | enclosing mark |
| Mn | non-spacing mark |
| N | number |
| Nd | decimal number |
| Nl | letter number |
| No | other number |
| P | punctuation |
| Pc | connector punctuation |
| Pd | dash punctuation |
| Pe | close punctuation |
| Pf | final punctuation |
| Pi | initial punctuation |
| Po | other punctuation |
| Ps | open punctuation |
| S | symbol |
| Sc | currency symbol |
| Sk | modifier symbol |
| Sm | math symbol |
| So | other symbol |
| Z | separator |
| Zl | line separator |
| Zp | paragraph separator |
| Zs | space separator |

| Unicode character class names--scripts |
| --- |
| Adlam |
| Ahom |
| Anatolian\_Hieroglyphs |
| Arabic |
| Armenian |
| Avestan |
| Balinese |
| Bamum |
| Bassa\_Vah |
| Batak |
| Bengali |
| Bhaiksuki |
| Bopomofo |
| Brahmi |
| Braille |
| Buginese |
| Buhid |
| Canadian\_Aboriginal |
| Carian |
| Caucasian\_Albanian |
| Chakma |
| Cham |
| Cherokee |
| Chorasmian |
| Common |
| Coptic |
| Cuneiform |
| Cypriot |
| Cyrillic |
| Deseret |
| Devanagari |
| Dives\_Akuru |
| Dogra |
| Duployan |
| Egyptian\_Hieroglyphs |
| Elbasan |
| Elymaic |
| Ethiopic |
| Georgian |
| Glagolitic |
| Gothic |
| Grantha |
| Greek |
| Gujarati |
| Gunjala\_Gondi |
| Gurmukhi |
| Han |
| Hangul |
| Hanifi\_Rohingya |
| Hanunoo |
| Hatran |
| Hebrew |
| Hiragana |
| Imperial\_Aramaic |
| Inherited |
| Inscriptional\_Pahlavi |
| Inscriptional\_Parthian |
| Javanese |
| Kaithi |
| Kannada |
| Katakana |
| Kayah\_Li |
| Kharoshthi |
| Khitan\_Small\_Script |
| Khmer |
| Khojki |
| Khudawadi |
| Lao |
| Latin |
| Lepcha |
| Limbu |
| Linear\_A |
| Linear\_B |
| Lisu |
| Lycian |
| Lydian |
| Mahajani |
| Makasar |
| Malayalam |
| Mandaic |
| Manichaean |
| Marchen |
| Masaram\_Gondi |
| Medefaidrin |
| Meetei\_Mayek |
| Mende\_Kikakui |
| Meroitic\_Cursive |
| Meroitic\_Hieroglyphs |
| Miao |
| Modi |
| Mongolian |
| Mro |
| Multani |
| Myanmar |
| Nabataean |
| Nandinagari |
| New\_Tai\_Lue |
| Newa |
| Nko |
| Nushu |
| Nyiakeng\_Puachue\_Hmong |
| Ogham |
| Ol\_Chiki |
| Old\_Hungarian |
| Old\_Italic |
| Old\_North\_Arabian |
| Old\_Permic |
| Old\_Persian |
| Old\_Sogdian |
| Old\_South\_Arabian |
| Old\_Turkic |
| Oriya |
| Osage |
| Osmanya |
| Pahawh\_Hmong |
| Palmyrene |
| Pau\_Cin\_Hau |
| Phags\_Pa |
| Phoenician |
| Psalter\_Pahlavi |
| Rejang |
| Runic |
| Samaritan |
| Saurashtra |
| Sharada |
| Shavian |
| Siddham |
| SignWriting |
| Sinhala |
| Sogdian |
| Sora\_Sompeng |
| Soyombo |
| Sundanese |
| Syloti\_Nagri |
| Syriac |
| Tagalog |
| Tagbanwa |
| Tai\_Le |
| Tai\_Tham |
| Tai\_Viet |
| Takri |
| Tamil |
| Tangut |
| Telugu |
| Thaana |
| Thai |
| Tibetan |
| Tifinagh |
| Tirhuta |
| Ugaritic |
| Vai |
| Wancho |
| Warang\_Citi |
| Yezidi |
| Yi |
| Zanabazar\_Square |

|&nbsp;| Vim character classes |
| --- | --- |
| \i | identifier character (NOT SUPPORTED) VIM |
| \I | \i except digits (NOT SUPPORTED) VIM |
| \k | keyword character (NOT SUPPORTED) VIM |
| \K | \k except digits (NOT SUPPORTED) VIM |
| \f | file name character (NOT SUPPORTED) VIM |
| \F | \f except digits (NOT SUPPORTED) VIM |
| \p | printable character (NOT SUPPORTED) VIM |
| \P | \p except digits (NOT SUPPORTED) VIM |
| \s | whitespace character (≡ [\t]) (NOT SUPPORTED) VIM |
| \S | non-white space character (≡ [^ \t]) (NOT SUPPORTED) VIM |
| \d | digits (≡ [0-9]) VIM |
| \D | not \d VIM |
| \x | hex digits (≡ [0-9A-Fa-f]) (NOT SUPPORTED) VIM |
| \X | not \x (NOT SUPPORTED) VIM |
| \o | octal digits (≡ [0-7]) (NOT SUPPORTED) VIM |
| \O | not \o (NOT SUPPORTED) VIM |
| \w | word character VIM |
| \W | not \w VIM |
| \h | head of word character (NOT SUPPORTED) VIM |
| \H | not \h (NOT SUPPORTED) VIM |
| \a | alphabetic (NOT SUPPORTED) VIM |
| \A | not \a (NOT SUPPORTED) VIM |
| \l | lowercase (NOT SUPPORTED) VIM |
| \L | not lowercase (NOT SUPPORTED) VIM |
| \u | uppercase (NOT SUPPORTED) VIM |
| \U | not uppercase (NOT SUPPORTED) VIM |
| \_x | \x plus newline, for any x (NOT SUPPORTED) VIM |
| \c | ignore case (NOT SUPPORTED) VIM |
| \C | match case (NOT SUPPORTED) VIM |
| \m | magic (NOT SUPPORTED) VIM |
| \M | nomagic (NOT SUPPORTED) VIM |
| \v | verymagic (NOT SUPPORTED) VIM |
| \V | verynomagic (NOT SUPPORTED) VIM |
| \Z | ignore differences in Unicode combining characters (NOT SUPPORTED) VIM |

| &nbsp; | Magic |
| --- | --- |
| (?{code}) | arbitrary Perl code (NOT SUPPORTED) PERL |
| (??{code}) | postponed arbitrary Perl code (NOT SUPPORTED) PERL |
| (?n) | recursive call to regexp capturing group n (NOT SUPPORTED) |
| (?+n) | recursive call to relative group +n (NOT SUPPORTED) |
| (?-n) | recursive call to relative group -n (NOT SUPPORTED) |
| (?C) | PCRE callout (NOT SUPPORTED) PCRE |
| (?R) | recursive call to entire regexp (≡ (?0)) (NOT SUPPORTED) |
| (?&amp;name) | recursive call to named group (NOT SUPPORTED) |
| (?P=name) | named backreference (NOT SUPPORTED) |
| (?P&gt;name) | recursive call to named group (NOT SUPPORTED) |
| (?(cond)true|false) | conditional branch (NOT SUPPORTED) |
| (?(cond)true) | conditional branch (NOT SUPPORTED) |
| (\*ACCEPT) | make regexps more like Prolog (NOT SUPPORTED) |
| (\*COMMIT) | (NOT SUPPORTED) |
| (\*F) | (NOT SUPPORTED) |
| (\*FAIL) | (NOT SUPPORTED) |
| (\*MARK) | (NOT SUPPORTED) |
| (\*PRUNE) | (NOT SUPPORTED) |
| (\*SKIP) | (NOT SUPPORTED) |
| (\*THEN) | (NOT SUPPORTED) |
| (\*ANY) | set newline convention (NOT SUPPORTED) |
| (\*ANYCRLF) | (NOT SUPPORTED) |
| (\*CR) | (NOT SUPPORTED) |
| (\*CRLF) | (NOT SUPPORTED) |
| (\*LF) | (NOT SUPPORTED) |
| (\*BSR\_ANYCRLF) | set \R convention (NOT SUPPORTED) PCRE |
| (\*BSR\_UNICODE) | (NOT SUPPORTED) PCRE |

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://github.com/google/re2/wiki/Syntax).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)