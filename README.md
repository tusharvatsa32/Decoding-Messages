## Problem:
The Ministry of Truth has intercepted a lengthy encrypted message from a subversive organization known by the codename Mammals of Insufferable Temperament (MIT). Because MIT lacks knowledge of modern cryptographic methods, they use simple substitution ciphers to encrypt messages. Those working for MIT speak an inelegant (but understandable) dialect of English. We have intercepted a message from MIT, the contents of which can be found in the file encoded.txt.
The task is to figure out the specific cipher used to create this encoded MIT document encoded.txt. Specifically, you will submit a key file key.txt , where each line contains two alphabet letters separated by a space. Substitution is performed on all 26 letters of the alphabet, for both capital letters and non-capital letters, so there should be a total of 52 lines in your key file. A useless but submittable key file has been provided for you as a template.

## Constraints:
The key file maps from the first column to the second column of letters. i.e. given the original plain text document, substituting letters from the first column with the respective letters from the second column will produce the encoded file. Uppercase letters should be mapped to uppercase letters, and lowercase letters should be mapped to lowercase letters. There is no cross-case substitution.Specifically, you can assume that the encoded document is sampled from the same distribution as the NYT data set, from which you can make some assumptions about the relative distribution of words and letters (we would expect it to be similar).

## My work flow:
1. Perform frequency analysis on the data from Part 1 and the encrypted message 

2. Improve key for some letters heuristically based on the frequency analysis

3. Attempt to decrypt the message using current mapping

4. Look at the output and manually refine the mappings, repeat step 2 to 4

## Challenges:
The frequency analysis part was confusing initially. Also, after refining the mappings there was some manual work which needed a lot of attention.

## File Description:
1.Encoded.txt- Contains the encoded text which we have to decipher.

2.decode.py- Contains the code for decrypting the encoded.txt

3.key.txt- Contains the mapping between different letters.

4.nyt.zip- Contains 1000 text files for frequency analysis
