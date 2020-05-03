# gdb
gdb is the 'GNU debugger', it's included in pretty much every unix distribution  

## running gdb 
```bash
g++ -g filename.cpp -o outputname # use the -g flag when compiling to give the debugger symbols
gdb outputname
```
this only starts the debugger, it does not run the program within the debugger
to start the program
```bash
(gdb) run # or shorthand
(gdb) r  
```

## important commands 
```bash
(gdb) next # step through program (skipping function calls) 
(gdb) n # ^
(gdb) step # step into function calls
(gdb) s # ^
(gdb) print var_name # print the current value of a variable called 'var_name' in the program
(gdb) bt # 'backtrace' gives useful info about where you are
(gdb) quit
```

## seg fault help
```bash 
    gdb filename core 
```
this will help with a segmentation fault (also called a core dump)

## breakpoints
```bash
    (gdb) b Line_number # e.g.
    (gdb) b 22
```
setting a breakpoint will mean the code will exit into the debugger at the set line

## want more?
```bash 
    man gdb 
    (gdb) help
```
