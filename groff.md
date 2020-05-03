# groff
groff is a minalist typesetting system for GNU/linux (all these commands are for the -ms bindings)

## compiling 
```groff
groff -e -ms -T pdf input.ms > output.pdf
```

## basic formatting 
```groff
.NH 
Creates a new header, title will be on this line 
.SH 
Creates a new header, no number
.PP
Is a paragraph, again on the newline, the next word will be 'bold'

.B "bold" !
.I "italics"
.BI "bold and italics"
.UL "underlined"
.BX "boxed"
```

## macros
```groff
.de NAME
.IP \(bu 2
..

```

## eqn 
```groff
.EQ
    x = 3 + 5
.EN
.EQ
    x sub 1 = y sup 2
.EN
.EQ
phi = {1 + sqrt 5} over 2
.EN
.EQ
s = sqrt {
    {sum from i=1 to N ( x sub i - x bar ) sup 2}
    over 
    {N-1}
}
.EN
.EQ
pi = integral from -1 to 1 dx over sqrt {1-x sup 2}
.EN

.EQ
delim $$
.EN

.PP
Here is an equation $sum from 1 to  10 = 5$
```
to use eqn make sure you compile with -e

## refer 
refer uses a reference file which lists the works the author might want to refer to
```groff
%K keyword  
%A author
%T title
%I publisher
%E editor
%D date
```
you can then refer to them
```groff
.[
    title author keyword
.]
```
you can use any of these or none of them 
```groff
refer -e file.ms | groff ...
```
you need to pipe the output of refer into the groff command  

## want to know more?
```bash
man groff
man eqn
man refer
```
