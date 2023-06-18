# Regex

`/<put pattern in here>/g` - basic structure for a regex, `g` means global

`[]` - match single character between brackets
`[^]` - don't match any of the characters between brackets
`[a-z]` - match single letter between a-z (case sensitive)
`[0-9]` - match single digit from 0-9

e.g. `/b[ae]r/g` will match *bar* and *ber* but not *bur* or *bir*

`{n}` - match an `n`-sized group of the preceding character or selector
`{n,}` - as above, but no upper limit (i.e. at least `n` in length)
`{n,m}` - as above, but between `n` and `m` in length

`.` - single character match, any letter or digit or symbol but not newline
`+` - one or more of preceding
`*` - zero or more of preceding
`?` - preceding is optional (zero or one)
`^` - range negation (or start of string depending on position), e.g. `[^b-d]`
`\` - escape, i.e. you want to match `*` and not use it as the 'zero or more' quantifier, use `\*`

`\d` - any digit
`\D` - any non-digit
`\w` - any word character (letter, digit and underscore, not whitespace)
`\W` - non of above
`\s` - any space character (inc. tabs)
`\t` - tabs only

`()` - a group, e.g. `book(.com)?` matches *book* and *book.com* as `.com` is made optional by grouping and using `?`
`|` - options in a group e.g. `bo(n|r)k` matches *bonk* and *bork*

`^` - match at start of string e.g. `^eck` will match *ecks* but not *feck*
`$` - match at end of string e.g. `boo$` will match *boo* and *sboo* but not *boos*

Recipes
- `/.{8}/g` matches any 'word' exactly 8 characters long
- `[a-zA-Z0-9]` matches all letters and digits, lower and upper case
- `[a-z]{4}` matches four letter words (lower case)
