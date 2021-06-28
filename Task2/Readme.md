## Task2
The crux in the problem is that FLAG,which is a string variable is declared inside secrets.jl file. <br>
So basically we need to reverse (inverse) the function f which is overloaded thrice.<br>
The first two instances of f are easily understandable and what the third instance does is as follows - <br>
Firstly it converts the string into a vector of data - type UInt8.<br>
Secondly it applies either of the two  initial f at all the index after converting them to Float64 and Int64 respectively.<br>
So in the final  output array if a number is even then dividing by 2 gives ascii of the original string, while if it is odd then that number subtracted by 1 and divided by 4.
