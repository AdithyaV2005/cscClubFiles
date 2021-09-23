# DATA REPRESENTATION 

## CONTENTS

1. ### Digital number system

   - Decimal number system
   - Binary number system
   - Octal number system
   - Hexadecimal number system

2. ### Number conversion

   - Decimal-binary
   - Binary-decimal
   - Decimal-octal
   - Octal-decimal
   - Octal-binary
   - Binary-octal
   - Decimal-hex
   - Hex-decimal

3. ### Binary addition

   - Basic cases
   - examples

4. ### Character/String representation

   - ASCII Code
   - ISCII Code
   - Unicode

### INTRO

- There are various number system being used . The most common number systems used are :

  1. Decimal
  2. Binary
  3. Octal
  4. Hexadecimal

  #### **DIGITAL NUMBER SYSTEM**S

1. Decimal number system
   - Deca means 10. So this system has 10 digits from 0-9.
   - The base of this number is 10
2. Binary number system
   - Bi means 2. uses only two digits and
   - Base is 2
   - weight expressed by powers of 2
3. Octal number system
   - Octa mean 8. Uses only eight digits from 0 - 7.
   - Base is 8
   - Weight expressed by the powers of 8
4. Hexadecimal number system
   - Hexa means 16. uses only 16 digits from 0-9 and from 10, 11,12, 13, 14, 15 the Corresponding alphabets are A, B. C, D, E and F.
   - Base is 16
   - Weight expressed by the power of 16

### NUMBER CONVERSION

1. **Decimal to binary**

   The common method of converting decimal to binary is repeated-division method. In this result is obtained by assembling all the remainders, with the last remainder being the most significant bit (MSB).

   ![Example for how to solve](https://cdn.programiz.com/sites/tutorial2program/files/decimal-to-binary-conversion_0.jpg)
2. **Binary to decimal**

   The binary number system is a positional system where each binary digit (bit) carries a certain weight based on its position relative to the LSB. Any binary number can be converted to its decimal equivalent simply by summing together the weights of the various positions in the binary number which contain a 1.

   ![Example how to solve](https://www.geeksforgeeks.org/wp-content/uploads/binary2decimal.png)
3. **Decimal to octal**

   A decimal integer can be converted to octal by using the same repeated-division method that we used in the decimal-to-binary conversion, but with a division factor of 8 instead of 2.

   ![Example how to solve](https://4.bp.blogspot.com/-nJlq9RNSsw4/XCZw_Bol7NI/AAAAAAAAATM/b4ZSUg7U2cYJrwsZ9rix1DlgOhQLVNUjgCLcBGAs/s1600/convert-decimal-to-octal-in-java.PNG)
4. **Octal to decimal**

   An octal number, then, can be easily converted to its decimal equivalent by multiplying each octal digit by its positional weight.

   ![Example how to solve](https://www.onlinemath4all.com/images/octal2decimal.png)
5. **Octal-to-Binary**

   The primary advantage of the octal number system is the ease with which conversion can be made between binary and octal numbers. The conversion from octal to binary is performed by converting each octal digit to its 3-bit binary equivalent.
6. **Binary to octal**

   Converting from binary integers to octal integers is simply the reverse of the foregoing process. The bits of the binary integer are grouped into groups of three bits starting at the LSB. Then each group is converted to its octal equivalent.

   ![Octal to binary and reverse](https://adamwsonu.files.wordpress.com/2010/02/oct2bin.png)
7. **Decimal to hex**

   Recall that we do decimal binary conversion using repeated division of 2 , and decimal octal conversion by dividing 8. Likewise, decimal to hex conversion could be done by repeated division of 16.

   ![Example for how to solve](https://worldtechjournal.com/wp-content/uploads/2021/04/decimal-to-hexadecimal-conversion-of-number-system-decimal-to-hexadecimal-hexadecimal-number-system-decimal-number-system-2.jpg)
8. ***Hex to decimal***

   A hex number can be converted to its decimal equivalent by using the fact that each hex digit position has a weight that is a power of 16. The LSD has a weight of 16^0 =1, the next higher digit has a weight of 16^1 =16, the next higher digit has a weight of 16^2 =256, and so on.

   ![Example for how to solve](https://i.ytimg.com/vi/70K48wueAQg/maxresdefault.jpg)

### BINARY ADDITION

- ALUs don't directly work upon decimal numbers ; rather they process binary numbers as a computer can understand only binary numbers. There are five basic cases for binary addition that must be understood before going on. These are :

1. **Case 1**
   - 0 + 0 = 0
2. **Case 2**
   - 1 + 0 = 1
3. **Case 3**
   - 0 + 1 = 1
4. **Case 4**
   - 1 + 1 = 10
5. **Case 5**
   - 1 + 1 + 1 = 11

![Example of binary addition](https://i2.wp.com/technobyte.org/wp-content/uploads/2020/01/Binary-Addition-Example-e1578686492368.jpg?ssl=1)

### CHARACTER / STRING REPRESENTATION

- The role of an encoding scheme is very crucial in computer system. Most popular encoding schemes are ASCII, Unicode, ISCII etc.

1. **ASCII CODE**

   The most widely used alphanumeric encoding scheme, the American Standard Code for Information Interchange (ASCII), is used in most microcomputers and minicomputers, and in many mainframes. The ASCII code (pronounced " askee") is a 7-bit code, and so it has 27 = 128 possible code groups.

   ![ASCII Code](https://i.ytimg.com/vi/H4l42nbYmrU/maxresdefault.jpg)
2. **ISCII CODE**

   With the advent of computerization considerable work has been undertaken to facilitate the use of Indian languages on computers. These activities were generally limited to specific languages and were independent exercises of various organizations, thus, making data-interchange impossible. In such a scenario, it was important to have a common standard for coding Indian scripts. In 1991, the Bureau of Indian Standards adopted the Indian Standard Code for Information Interchange (ISCII), the ISCII standard that was evolved by a standardization committee. This is an eight-bit code capable of coding 256 characters. ISCII code retains all ASCII characters and offers coding for Indian scripts also. Thus, it is also called Indian Scripts Code for Information Interchange.

   ![Example of ISCII CODE](https://nirav.com.np/uploads/codepoint_table.png)

3. **UNICODE**

   - Unicode has been developed as a universal character set with an aim:

     1. To define all the characters needed for writing the majority of known languages in use on computers in one place.
     2. To be a superset of all other character sets that have been encoded.

     ![Example of Unicode table](https://i.insider.com/567ea534e6183e26008b4f0e)

# THANK YOU!