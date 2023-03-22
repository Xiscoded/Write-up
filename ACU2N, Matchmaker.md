# Write up for challenge : ACU2N, Matchmaker
## Instruction
There are a variety of symmetric cryptosystems out there, but most of them involve a logic block called a XOR. The key is "hab"(UTF8). We're giving you the key and the algorithm, how hard can it be?

Dg0DDxoRBz4PHQIKNxIbBQwHHBMbFQ==

*external ressources* : [here](https://qualifier.hackabit.com/learning/acu2n-matchmaker)
## Solution
We notice that "Dg0DDxoRBz4PHQIKNxIbBQwHHBMbFQ==" could be encoded with Base64. So we are going to use CyberChef ([cyberchef.org](https://cyberchef.org)) to convert "Dg0DDxoRBz4PHQIKNxIbBQwHHBMbFQ==
" into plaintext, we use the "From Base64" block in the recipe column and we paste the encoded text in the input section, which gives the output :</br>
**. </br>
.....>... </br>
7.........** </br>
We then need to convert the output into binary to perform the XOR operation. We now use the "To Binary" block, which gives the following output :</br>
**00001110 00001101 00000011 00001111 00011010 00010001 00000111 00111110 00001111 00011101 00000010 00001010 00110111 00010010 00011011 00000101 00001100 00000111 00011100 00010011 00011011 00010101** </br>

Now, we use the site [https://www.dcode.fr/xor-cipher](https://https://www.dcode.fr/xor-cipher) to calculate the XOR operation between our binary number and the key that was given to us at the begining. We 
paste the binary into the "Text to be XORed (multiplied by XOR)" section, we then select the "Use the ascii key" button with the value set to "**hab**" and finally we select the "ASCII (printable) characters" button in the "Results format" section.</br>
Clicking on "Decrypt" gives the following result : **flag{so_much_symmetry}**
