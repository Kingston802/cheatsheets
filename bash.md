# bash
bash (bourne again shell) aka GNU bash is a unix shell and command language written by brian fox, it's kind of everywhere

## control structures 
luke smith says don't use if statements ok?
```bash
case "$Variable$" in 
    0) command;;
    1) command;;
    *) default;;
esac

for Variable in {1..3}
do
    echo "$Variable"
done

function foo ()
{
    return 0
}
foo arg1 arg2

if [ $var != $condition ]
then
    echo "something"
else
    echo "something else"
fi
```

## important commands 
```bash
echo 'some text that will be output'
grep 'searchText'
```

<!-- ## -->  
<!-- ```bash -->

<!-- ``` -->

## need more help?
```bash
man bash 
info bash
```
