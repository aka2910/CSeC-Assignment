## Task2
The crux in the problem is that `FLAG`, is a string variable is declared inside `secrets.jl` file. <br>
Basically we need to reverse (inverse) the function f which is overloaded thrice to get the value of `FLAG`.<br>
The first two instances of the function f are easily understandable.
And what the third instance of the function does is as follows - <br>
> - Firstly it converts the input string into a vector named s of datatype - UInt8 i.e. all the chars of the string to a vector of there ASCII in Hex.
> - Then it creates a variable x which contains a sublist of index of the vector. (PS - Julia array are 1 indexed, also randsubseq gives ordered sublist)
> - Also it creates a variable y which conntains the remaining indices not included in x.
> - Then a vector named o of length equal to length of stting is created with uninitialised value.
> - At indexes corresponding to x we store corresponding elements of s converted to Float64 similary as Int64 for y.
> - Now at all the position the intital two f are applied according to Int or Float.
> - we get an odd number((this-1)/4 gives us ASCII) when the entry in o was Float and an even number when the entry was Int(this/2 gives us ASCII).

The python script for the same is below - 
```
arr = [204, 216, 389, 413, 493, 437, 234, 197, 465, 421, 224, 433, 205, 381, 401, 421, 213,
       449, 209, 232, 198, 208, 381, 98, 461, 190, 209, 477, 202, 213, 193, 437, 405, 250]
ans = ''
for i in arr:
    ans += chr(int(i/2)) if i % 2 == 0 else chr(int((i-1)/4))
print(ans)

```
### Answer
**flag{mu1tipl3_di5p4tch_1s_4we50me}**
