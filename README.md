# test-regex
A website to test your regex:
[REGEXR](https://regexr.com/)
## Sample regex to easily edit CORNER files. You can change the number inside the curly braces to match the column you want then replace it using `sed`.
- Regular expression to match column of text/numbers in a corner file using extended regular expression: `(?<=^(\S+\s){8}).`
- The first regex matches beginning of line with no white space then a white space.
- It is enclosed inside a capture group to implement same rules to it `(^\S+\s)`.
- A rule is implemented to the regex inside the capture group, that is match it 8 times using `{8}`.
- A look behind is used to match any character(represented by `.`) preceded by the regex pattern.

## The replace can also be implemented using sed without using look-behind by using \1 to keep part of the pattern.
Like so:
`sed -r 's:(^(\S+\s){9}).:\12:gm' corners.txt`
