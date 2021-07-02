## Task 3
My initially thought to  this problem was that, the given audio has 2 phrases so I thought of converting them to 0 and 1.<br>
The string that I got initially was `110100011101010110010000110001011011110101111101101001001101010101111101101110001100010110001100110011` or it's complement.<br>
As this one is having length 102 and `102%8 =\= 0`. So I couldn't proceed much. I also tried Audacity/ Deepsound but they were useless.<br>
After the realease of hint-1 my logic was confirmed but still I couldn't do much.<br>
When the 2nd hint was released the audio had two more zeros at the beginning and this one worked perfectly. Though I expected the `flag{...}` format but it directly had the value of flag.<br>
The reason for this could be that the problem statement never talked about flag and just said that there is a secret message.<br>
In the initial audio I should have tried concatenating two zeros at the left but this idea didn't strike me :'( <br>
So finally the string was `00110100011101010110010000110001011011110101111101101001001101010101111101101110001100010110001100110011` and below is the script I used. <br>
```
var = '00110100011101010110010000110001011011110101111101101001001101010101111101101110001100010110001100110011'
ans = ''
for i in range(0, len(var), 8):
    ans += chr(int(var[i:i+8], 2))
print(ans)
```
### Final Answer
`4ud1o_i5_n1c3`
