# mada_huffman_bonus_assignment
Programming assignment Huffman

Write a program in Java that is capable of the following:
1. A text file (ASCII) is to be read in.
2. Create a frequency table for the symbols of the file. (Hint: (int) c yields the ASCII value
of a character c).
3. Construct a Huffman code from this table.
4. Store the Huffman table in an external file dec tab.txt in the form: ASCII code of
symbol1:code of symbol1-ASCII code of symbol2:code of symbol 2- . . .
5. The string that has been read in should be converted into a bit string using the Huffman
code.
6. Append a 1 and afterwards 0s until the length of the string is divisible by 8.
7. Convert this (extended) bit string into a byte array by combining each 8 subsequent bits
to a byte.
8. Store this byte array in an external file output.dat. (Hint:
```Java
FileOutputStream fos = new FileOutputStream("output.dat");
fos.write(out);
fos.close();

// writes the byte array out to output.dat,

File file = new File("output.dat");
byte[] bFile = new byte[(int) file.length()];
FileInputStream fis = new FileInputStream(file);
fis.read(bFile);
fis.close();
``` 
reads it in.)

9. The program should be able to decode. That is: The code table and a byte array should
be read in from external files. The byte array is converted into a bit string from which the
last 1 and all subsequent 0s are removed. The remaining bit string is then to be decoded
using the code table and to be stored in an external file decompress.txt.
10. Test your program on several text files and observe how much storage space is saved.
11. Decode output-mada.dat with dec tab-mada.txt.


General notes:
1. You can work in groups of at most 3 people.
2. A complete solution yields a bonus of 0.3 on the grade of the second assessment. (The
final continuous assessment grade is, for technical reasons, between 1.0 and 6.0.)
3. Include the result of the decoding of output-mada.dat with dec tab-mada.txt in
your email!
4. The program should be comprehensibly commented.
5. You do not need an advanced knowledge of object-oriented programming. It is indeed not
necessary (but you are allowed) to write or use a class for a tree. (The Huffman code can
be constructed with just a few arrays).
6. You will need some functions for handling strings in java. A short overview can be found
here: http://www.tutorialspoint.com/java/java_strings.htm.
7. I assume that, for fairness reasons, you do not try to cheat. However I will also check this
with tools. If I detect an attempt to deceive by submitting (disguised) copies of parts of
existing programs, taken from the Internet or fellow students, I will set the grade of the
next assessment to 1.0.
