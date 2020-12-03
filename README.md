# start
1.WAP to count no of digits in a number .
#include <stdio.h>

int main()
{
     int n;  
   int count=0;   
   printf("Enter a number");  
   scanf("%d",&n);  
   while(n!=0)  
   {  
       n=n/10;  
       count++;  
   }  
     
   printf("\nThe number of digits in an integer is : %d",count);  

    return 0;
}
Enter a number56                                                                                                                              
                                                                                                                                              
The number of digits in an integer is : 2                                                                                                     
                                                                                                                                              
...Program finished with exit code 0                                                                                                          
Press ENTER to exit console. 

2.WAP to swap first and last digit of a number.
#include <stdio.h>

int main()
{
    int num, last, first, temp, swap, count = 0;
 
    printf("Enter any number: ");
    scanf("%d", &num);
 
    temp = num;
    last = temp % 10;
    count = (int)log10(temp);
 
    while(temp>=10)
    {
        temp /= 10;
    }
    first = temp;
    swap = (last * pow(10, count) + first) + (num - (first * pow(10, count) + last));
 
    printf("Last Digit: %d\n", last);
 
    printf("First Digit: %d\n", first);
 
    printf("%d is swapped to %d\n", num, swap);


    return 0;
}
Enter any number: 56                                                                                                                            
Last Digit: 6                                                                                                                                   
First Digit: 5                                                                                                                                  
56 is swapped to 65                                                                                                                             
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.  

3.WAP to find frequency of each digit in a given integer .
#include <stdio.h>

int main()
{
    long num;

    int digit,rem,count=0;

    printf("Enter the Number: ");

    scanf("%ld",&num);

    printf("Enter the digit to be counted:");

    scanf("%d",&digit);

    while(num!=0)
    {

       rem=num%10;

       if(rem==digit)
        
       count++;
       
       num=num/10;
    }

printf("The digit %d present %d times ",digit,count);

    return 0;
}
Enter the Number: 58699                                                                                                                       
Enter the digit to be counted:9                                                                                                               
The digit 9 present 2 times                                                                                                                   
                                                                                                                                              
...Program finished with exit code 0                                                                                                          
Press ENTER to exit console.    

4.WAP to enter a no and print in words.
#include <stdio.h>

int main()
{
   int data, num = 0, digits;

    printf("Enter any number to print in words: ");
    scanf("%d", &data);

    digits = (int) log10(data);
    
    while(data != 0)
    {
        num = (num * 10) + (data % 10);
        data /= 10;
    }
    
    digits =  digits - ((int) log10(num));

    while(num != 0)
    {
        switch(num % 10)
        {
        case 0:
            printf("Zero ");
            break;
        case 1:
            printf("One ");
            break;
        case 2:
            printf("Two ");
            break;
        case 3:
            printf("Three ");
            break;
        case 4:
            printf("Four ");
            break;
        case 5:
            printf("Five ");
            break;
        case 6:
            printf("Six ");
            break;
        case 7:
            printf("Seven ");
            break;
        case 8:
            printf("Eight ");
            break;
        case 9:
            printf("Nine ");
            break;
        }
        num /= 10;
    }
    
    while(digits)
    {
        printf("Zero ");
        digits--;
    }


    return 0;
}
Enter any number to print in words: 255                                                                                                         
Two Five Five                                                                                                                                   
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.            

5.WAP to print all ASCII characters with their values .
#include <stdio.h>

int main()
{
    int i;
  
  	for(i = 65; i <= 90; i++)
   	{
    	printf("The ASCII value of %c = %d\n", i, i);
   	}

    return 0;
}
The ASCII value of A = 65                                                                                                                       
The ASCII value of B = 66                                                                                                                       
The ASCII value of C = 67                                                                                                                       
The ASCII value of D = 68                                                                                                                       
The ASCII value of E = 69                                                                                                                       
The ASCII value of F = 70                                                                                                                       
The ASCII value of G = 71                                                                                                                       
The ASCII value of H = 72                                                                                                                       
The ASCII value of I = 73                                                                                                                       
The ASCII value of J = 74                                                                                                                       
The ASCII value of K = 75                                                                                                                       
The ASCII value of L = 76                                                                                                                       
The ASCII value of M = 77                                                                                                                       
The ASCII value of N = 78                                                                                                                       
The ASCII value of O = 79                                                                                                                       
The ASCII value of P = 80                                                                                                                       
The ASCII value of Q = 81                                                                                                                       
The ASCII value of R = 82                                                                                                                       
The ASCII value of S = 83                                                                                                                       
The ASCII value of T = 84                                                                                                                       
The ASCII value of U = 85                                                                                                                       
The ASCII value of V = 86                                                                                                                       
The ASCII value of W = 87                                                                                                                       
The ASCII value of X = 88                                                                                                                       
The ASCII value of Y = 89                                                                                                                       
The ASCII value of Z = 90              

6.WAP to find one’s compliment of a binary number.
 #include <stdio.h>

int main()
{
    #define SIZE 8
    
    char binary[SIZE + 1], onesComp[SIZE + 1];
    int i, error=0;

    printf("Enter %d bit binary value: ", SIZE);
   
    gets(binary);
    for(i=0; i<SIZE; i++)
    {
        if(binary[i] == '1')
        {
            onesComp[i] = '0';
        }
        else if(binary[i] == '0')
        {
            onesComp[i] = '1';
        }
        else
        {
            printf("Invalid Input");
            error = 1;

            break;
        }
    }
    
    onesComp[SIZE] = '\0';

    if(error == 0)
    {
        printf("Original binary = %s\n", binary);
        printf("Ones complement = %s", onesComp);
    }

    return 0;
}
Enter 8 bit binary value: 11111010                                                                                                              
Original binary = 11111010                                                                                                                      
Ones complement = 00000101                                                                                                                      
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                              

7.WAP to print two’s compliment of a binary number.
#include <stdio.h>

int main()
{
    char binaryNumber[100], onesComplement[100], twosComplement[100];
    int counter, error=0, digitCount, carry = 1;   
    
    printf("Enter a Binary Number\n");  
    scanf("%s", binaryNumber);  
   

    digitCount = strlen(binaryNumber);
     
 for(counter=0; counter < digitCount; counter++) {  
        if(binaryNumber[counter]=='1') {  
            onesComplement[counter] = '0';  
        } else if(binaryNumber[counter]=='0') {  
            onesComplement[counter] = '1';  
        } else {  
            printf("Error :( ");  
            return 1;
        }  
    }  
    onesComplement[digitCount] = '\0';
     

    for(counter = digitCount-1; counter >= 0; counter--) {  
        if(onesComplement[counter]=='1' && carry==1){
            twosComplement[counter] = '0';  
        } else if(onesComplement[counter]=='0' && carry==1) {  
            twosComplement[counter] = '1';  
            carry = 0;  
        } else {  
            twosComplement[counter] = onesComplement[counter];  
        }  
    }  
    twosComplement[digitCount] = '\0'; 
       
    printf("Two's Complement : %s", twosComplement);  
   
    


    return 0;
}
Enter a Binary Number                                                                                                                           
0101                                                                                                                                            
Two's Complement : 1011                                                                                                                         
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                              

8. WAP to convert binary to octal number system.
#include <stdio.h>

int main()
{
    long int binarynum, octalnum = 0, j = 1, remainder;
 
    printf("Enter the value for  binary number: ");
    scanf("%ld", &binarynum);
    while (binarynum != 0)
    {
        remainder = binarynum % 10;
        octalnum = octalnum + remainder * j;
        j = j * 2;
        binarynum = binarynum / 10;
    }
    printf("Equivalent octal value: %lo", octalnum);

    return 0;
}
Enter the value for  binary number: 11010                                                                                                       
Equivalent octal value: 32                                                                                                                      
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                                 

9. WAP to convert binary to decimal number system.
#include <stdio.h>

int main()
{
    int  num, binary_val, decimal_val = 0, base = 1, rem;
 
    printf("Enter a binary number(1s and 0s) \n");
    scanf("%d", &num); 
    binary_val = num;
    while (num > 0)
    {
        rem = num % 10;
        decimal_val = decimal_val + rem * base;
        num = num / 10 ;
        base = base * 2;
    }
    printf("The Binary number is = %d \n", binary_val);
    printf("Its decimal equivalent is = %d \n", decimal_val);

    return 0;
}
Enter a binary number(1s and 0s)                                                                                                                
111                                                                                                                                             
The Binary number is = 111                                                                                                                      
Its decimal equivalent is = 7                                                                                                                   
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.             

10. WAP to convert binary to hexadecimal number system.
#include <stdio.h>

int main()
{
   long int binaryval, hexadecimalval = 0, i = 1, remainder;
 
    printf("Enter the binary number: ");
    scanf("%ld", &binaryval);
    while (binaryval != 0)
    {
        remainder = binaryval % 10;
        hexadecimalval = hexadecimalval + remainder * i;
        i = i * 2;
        binaryval = binaryval / 10;
    }
    printf("Equivalent hexadecimal value: %lX", hexadecimalval);

    return 0;
}
Enter the binary number: 1111                                                                                                                   
Equivalent hexadecimal value: F                                                                                                                 
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                                        

11. WAP to convert octal to binary number system.
#include <stdio.h>
#define MAX 100
int main()
{
    char octalnum[MAX];
    long i = 0;
 
    printf("Enter any octal number: ");
    scanf("%s", octalnum);
    printf("Equivalent binary value: ");
    while (octalnum[i])
    {
        switch (octalnum[i])
        {
        case '0':
            printf("000"); break;
        case '1':
            printf("001"); break;
        case '2':
            printf("010"); break;
        case '3':
            printf("011"); break;
        case '4':
            printf("100"); break;
        case '5':
            printf("101"); break;
        case '6':
            printf("110"); break;
        case '7':
            printf("111"); break;
         default:
            printf("\n Invalid octal digit %c ", octalnum[i]);
            return 0;
        }
        i++;
    }
    return 0;

    return 0;
}
Enter any octal number: 56                                                                                                                      
Equivalent binary value: 101110                                                                                                                 
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.          

12. WAP to convert octal to decimal number system.
#include <stdio.h>

int main()
{
    long int octal, decimal = 0;
    int i = 0;
 
    printf("Enter any octal number: ");
    scanf("%ld", &octal);
    while (octal != 0)
    {
        decimal =  decimal +(octal % 10)* pow(8, i++);
        octal = octal / 10;
    }
    printf("Equivalent decimal value: %ld",decimal);

    return 0;
}
Enter any octal number: 56                                                                                                                      
Equivalent decimal value: 46                                                                                                                    
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.  

13. WAP to convert octal to hexadecimal number system.
#include <stdio.h>

int main()
{
    int octaltobinary[]={0,1,10,11,100,101,110,111};  
  char hexadecimal[10];  
   char hex[10];  
  long int binary=0;  
  int octal;  
  int rem=0;  
  int position=1;  
  int len=0;  
   int k=0;  
  printf("Enter a octal number ");  
  scanf("%d",&octal);  

while(octal!=0)  
  {  
      rem=octal%10;  
      binary=octaltobinary[rem]*position+binary;  
      octal=octal/10;  
      position=position*1000;  
  }  
  printf("The binary number is : %ld",binary);  
    
  while(binary > 0)  
    {  
        rem = binary % 10000;  
        switch(rem)  
        {  
            case 0:  
                strcat(hexadecimal, "0");  
                break;  
            case 1:  
                strcat(hexadecimal, "1");  
                break;  
            case 10:  
                strcat(hexadecimal, "2");  
                break;  
            case 11:  
                strcat(hexadecimal, "3");  
                break;  
            case 100:  
                strcat(hexadecimal, "4");  
                break;  
            case 101:  
                strcat(hexadecimal, "5");  
                break;  
            case 110:  
                strcat(hexadecimal, "6");  
                break;  
            case 111:  
                strcat(hexadecimal, "7");  
                break;  
            case 1000:  
                strcat(hexadecimal, "8");  
                break;  
            case 1001:  
                strcat(hexadecimal, "9");  
                break;  
            case 1010:  
                strcat(hexadecimal, "A");  
                break;  
            case 1011:  
                strcat(hexadecimal, "B");  
                break;  
            case 1100:  
                strcat(hexadecimal, "C");  
                break;  
            case 1101:  
                strcat(hexadecimal, "D");  
                break;  
            case 1110:  
                strcat(hexadecimal, "E");  
                break;  
            case 1111:  
                strcat(hexadecimal, "F");  
            break;  
        }  
len=len+1;  
        binary /= 10000;  
    }  
  for(int i=len-1;i>=0;i--)  
{  
    hex[k]=hexadecimal[i];  
    k++;  
}  
hex[len]='\0';  
printf("\nThe hexadecimal number is :");  
for(int i=0; hex[i]!='\0';i++)  
{  
    printf("%c",hex[i]);  
}  

    return 0;
}
Enter a octal number 65                                                                                                                         
The binary number is : 110101                                                                                                                   
The hexadecimal number is :35                                                                                                                   
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    

14. WAP to convert decimal to binary number system.
#include <stdio.h>

int main()
{
   int number, n, remainder, binary = 0, place = 1;

    printf("Enter a number :");
    scanf("%d", &number);

    n = number;

    while (n > 0)
    {
        remainder = n % 2;
        binary += remainder * place;
        place *= 10;
        n /= 2;
    }
    
    printf("Binary equivalent of %d is %d", number, binary);

    return 0;
}
Enter a number :7                                                                                                                               
Binary equivalent of 7 is 111                                                                                                                   
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                                       

15. WAP to convert decimal to octal number system.
#include <stdio.h>

int main()
{
   int octalNumber[10], number, i, j;
    printf("\n Please Enter the Number You want to Convert  :  ");
    scanf("%d", &number);
    
    for(i = 0; number > 0; i++)
    {
        octalNumber[i] = number % 8;
        number = number / 8;
    }
    
    printf("\n Equivalent Octal Number of a Given Number =  ");
    for(j = i - 1; j >= 0; j--)  
    {
        printf("%d", octalNumber[j]);
    }
    return 0;
}
Please Enter the Number You want to Convert  :  56                                                                                             
                                                                                                                                                
 Equivalent Octal Number of a Given Number =  70                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.  

16. WAP to convert decimal to hexadecimal number system.
#include <stdio.h>

int main()
{
    long int decimalNumber,remainder,quotient;
	int i=1,j,temp;
	char hexadecimalNumber[100];
	printf("Enter any decimal number: ");
	scanf("%ld",&decimalNumber);
	quotient = decimalNumber;
	while(quotient!=0) {
		temp = quotient % 16;
		
		if( temp < 10)
		           temp =temp + 48; else
		         temp = temp + 55;
		hexadecimalNumber[i++]= temp;
		quotient = quotient / 16;
	}
	printf("Equivalent hexadecimal value of decimal number %d: ",decimalNumber);
	for (j = i -1 ;j> 0;j--)
	      printf("%c",hexadecimalNumber[j]);

    return 0;
}
Enter any decimal number: 455                                                                                                                   
Equivalent hexadecimal value of decimal number 455: 1C7                                                                                         
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.   

17. WAP to convert hexadecimal  to binary number system.
#include <stdio.h>
#define MAX 100
int main()
{
    char binarynum[MAX], hexa[MAX];
    long int i = 0;
 
    printf("Enter the value for hexadecimal ");
    scanf("%s", hexa);
    printf("\n Equivalent binary value: ");
    while (hexa[i])
    {
        switch (hexa[i])
        {
        case '0':
            printf("0000"); break;
        case '1':
            printf("0001"); break;
        case '2':
            printf("0010"); break;
        case '3':
            printf("0011"); break;
        case '4':
            printf("0100"); break;
        case '5':
            printf("0101"); break;
        case '6':
            printf("0110"); break;
        case '7':
            printf("0111"); break;
        case '8':
            printf("1000"); break;
        case '9':
            printf("1001"); break;
        case 'A':
            printf("1010"); break;
        case 'B':
            printf("1011"); break;
        case 'C':
            printf("1100"); break;
        case 'D':
            printf("1101"); break;
        case 'E':
            printf("1110"); break;
        case 'F':
            printf("1111"); break;
        case 'a':
            printf("1010"); break;
        case 'b':
            printf("1011"); break;
        case 'c':
            printf("1100"); break;
        case 'd':
            printf("1101"); break;
        case 'e':
            printf("1110"); break;
        case 'f':
            printf("1111"); break;
        default:
            printf("\n Invalid hexa digit %c ", hexa[i]);
            return 0;
        }
        i++;
    }

    return 0;
}
Enter the value for hexadecimal 565                                                                                                             
                                                                                                                                                
 Equivalent binary value: 010101100101                                                                                                          
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                                 

18. WAP to convert hexadecimal  to octal number system.
#include <stdio.h>

int main()
{
    int hexDigitToBinary[16] = {0, 1, 10, 11, 100, 101, 110, 111,
      1000, 1001, 1010, 1011, 1100, 1101, 1110, 1111};     
    char hexDigits[16] = {'0', '1', '2', '3', '4', '5', '6', '7',
      '8', '9', 'A', 'B', 'C', 'D', 'E', 'F'};
    int octalDigitToBinary[8] = {0,1,10,11,100,101,110,111}; 
    char hexadecimal[30];
    long long binaryNumber =0, octalNumber;   
    int i = 0, j, index=0, multiple = 1, threeDigits;  
  
    printf("Enter a Hexadecimal Number\n");  
    scanf("%s", hexadecimal);
    
    
    
    for(i=0; hexadecimal[i] != '\0'; i++)  {  
        
        for(j = 0; j < 16; j++){
          if(hexDigits[j] == hexadecimal[i]){
            binaryNumber = binaryNumber*10000 + hexDigitToBinary[j];
          }
        }
    }  
    
    while(binaryNumber != 0) {  
        threeDigits = binaryNumber % 1000;
        
        for(i = 0; i < 8; i++) {  
            if(octalDigitToBinary[i] == threeDigits) {  
                octalNumber = (i * multiple) + octalNumber;  
                break;  
            }  
        }  
    
        binaryNumber = binaryNumber/1000;  
        multiple *= 10;  
    }  
    printf("Octal number : %ld", octalNumber);  
  

    return 0;
}
Enter a Hexadecimal Number                                                                                                                      
6556                                                                                                                                            
Octal number : 62526                                                                                                                            
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.  

19. WAP to convert hexadecimal  to decimal number system.
#include <stdio.h>

int main()
{
    int decimal_number = 0, remainder, hexadecimal_number;
      int count = 0;
      printf("Enter a Hexadecimal Number:\t");
      scanf("%d", &hexadecimal_number); 
      while(hexadecimal_number > 0)
      {
            remainder = hexadecimal_number % 10;
            decimal_number = decimal_number + remainder * pow(16, count);
            hexadecimal_number = hexadecimal_number / 10;
            count++;
      }
      printf("\nDecimal Equivalent:\t%d\n", decimal_number);

    return 0;
}
Enter a Hexadecimal Number:     5656                                                                                                            
                                                                                                                                                
Decimal Equivalent:     22102                                                                                                                   
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.       

1.WAP to print following star patters.
Pyramid star pattern
#include <stdio.h>

int main()
{
   int i, space, rows, k = 0;
   printf("Enter the number of rows: ");
   scanf("%d", &rows);
   for (i = 1; i <= rows; ++i, k = 0) {
      for (space = 1; space <= rows - i; ++space) {
         printf("  ");
      }
      while (k != 2 * i - 1) {
         printf("* ");
         ++k;
      }
      printf("\n");
   }

    return 0;
}
Enter the number of rows: 5                                                                                                                     
        *                                                                                                                                       
      * * *                                                                                                                                     
    * * * * *                                                                                                                                   
  * * * * * * *                                                                                                                                 
* * * * * * * * *                                                                                                                               
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.          

Inverted pyramid star pattern 
#include <stdio.h>

int main()
{
    int rows, i, j, space;
   printf("Enter the number of rows: ");
   scanf("%d", &rows);
   for (i = rows; i >= 1; --i) {
      for (space = 0; space < rows - i; ++space)
         printf("  ");
      for (j = i; j <= 2 * i - 1; ++j)
         printf("* ");
      for (j = 0; j < i - 1; ++j)
         printf("* ");
      printf("\n");
   }

    return 0;
}
Enter the number of rows:                                                                                                                       
5                                                                                                                                               
* * * * * * * * *                                                                                                                               
  * * * * * * *                                                                                                                                 
    * * * * *                                                                                                                                   
      * * *                                                                                                                                     
        *                                                                                                                                       
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.             
Hollow pyramid star pattern
#include <stdio.h>

int main()
{
    int i, j, rows;

    printf("Enter number of rows : ");
    scanf("%d", &rows);

    for(i=1; i<=rows; i++)
    {
        for(j=i; j<rows; j++)
        {
            printf(" ");
        }
        for(j=1; j<=(2*i-1); j++)
        {
            if(i==rows || j==1 || j==(2*i-1))
            {
                printf("*");
            }
            else
            {
                printf(" ");
            }
        }
        printf("\n");
    }

    return 0;
}
Enter number of rows : 5                                                                                                                        
    *                                                                                                                                           
   * *                                                                                                                                          
  *   *                                                                                                                                         
 *     *                                                                                                                                        
*********                                                                                                                                       
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.        

Hollow inverted pyramid star pattern
#include <stdio.h>

int main()
{
    int i, j, rows;

    printf("Enter number of rows: ");
    scanf("%d", &rows);

    for(i=1; i<=rows; i++)
    {
        for(j=1; j<i; j++)
        {
            printf(" ");
        }

        for(j=1; j<=(rows*2 - (2*i-1)); j++)
        {
        
            if(i==1 || j==1 || j==(rows*2 - (2*i - 1)))
            {
                printf("*");
            }
            else
            {
                printf(" ");
            }
        }
    
        printf("\n");
    }

    return 0;
}
Enter number of rows: 5                                                                                                                         
*********                                                                                                                                       
 *     *                                                                                                                                        
  *   *                                                                                                                                         
   * *                                                                                                                                          
    *                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                                  

Half diamond star pattern
#include <stdio.h>

int main()
{
    int number, i, k, count = 1;
 
    printf("Enter number of rows\n");
    scanf("%d", &number);
    count = number - 1;
    for (k = 1; k <= number; k++)
    {
        for (i = 1; i <= count; i++)
            printf(" ");
        count--;
        for (i = 1; i <= 2 * k - 1; i++)
            printf("*");
        printf("\n");
     }
     count = 1;
     for (k = 1; k <= number - 1; k++)
     {
         for (i = 1; i <= count; i++)
             printf(" ");
         count++;
         for (i = 1 ; i <= 2 *(number - k)-  1; i++)
             printf("*");
         printf("\n");
      }
    return 0;
}
Enter number of rows                                                                                                                            
5                                                                                                                                               
    *                                                                                                                                           
   ***                                                                                                                                          
  *****                                                                                                                                         
 *******                                                                                                                                        
*********                                                                                                                                       
 *******                                                                                                                                        
  *****                                                                                                                                         
   ***                                                                                                                                          
    *                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.               
2.WAP to print tne given number pattern.
Square number pattern
#include <stdio.h>

int main()
{
    int rows, cols, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    printf("Enter number of columns: ");
    scanf("%d", &cols);

    for(i=1; i<=rows; i++)
    {
        for(j=1; j<=cols; j++)
        {
            printf("1");
        }

        printf("\n");
    }

    return 0;
}
Enter number of rows: 5                                                                                                                         
Enter number of columns: 5                                                                                                                      
11111                                                                                                                                           
11111                                                                                                                                           
11111                                                                                                                                           
11111                                                                                                                                           
11111                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.               

Number pattern 1
#include <stdio.h>

int main()
{
    int rows, cols, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    printf("Enter number of columns: ");
    scanf("%d", &cols);

    for(i=1; i<=rows; i++)
    {
        for(j=1; j<=cols; j++)
        {
            if(i%2 == 1)
            {
                printf("1");
            }
            else
            {
                printf("0");
            }
        }

        printf("\n");
    }

    return 0;
}
Enter number of rows: 5                                                                                                                         
Enter number of columns: 5                                                                                                                      
11111                                                                                                                                           
00000                                                                                                                                           
11111                                                                                                                                           
00000                                                                                                                                           
11111                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.           

Number pattern 2
#include <stdio.h>

int main()
{
    int rows, cols, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    printf("Enter number of columns: ");
    scanf("%d", &cols);

    for(i=1; i<=rows; i++)
    {
        for(j=1; j<=cols; j++)
        {
            if(j%2 == 1)
            {
                printf("0");
            }
            else
            {
                printf("1");
            }
        }

        printf("\n");
    }

    return 0;
}
Enter number of rows: 5                                                                                                                         
Enter number of columns: 5                                                                                                                      
01010                                                                                                                                           
01010                                                                                                                                           
01010                                                                                                                                           
01010                                                                                                                                           
01010                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.           

Number pattern 3
#include <stdio.h>

int main()
{
    int rows, cols, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    printf("Enter number of columns: ");
    scanf("%d", &cols);

    for(i=1; i<=rows; i++)
    {
        for(j=1; j<=cols; j++)
        {
            if(i==1 || i==rows || j==1 || j==cols)
            {
                printf("1");
            }
            else
            {
                printf("0");
            }
        }

        printf("\n");
    }


    return 0;
}
Enter number of rows: 5                                                                                                                         
Enter number of columns: 5                                                                                                                      
11111                                                                                                                                           
10001                                                                                                                                           
10001                                                                                                                                           
10001                                                                                                                                           
11111                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.          

Number pattern 4
#include <stdio.h>

int main()
{
    int rows, cols, i, j;
    int centerRow, centerCol;
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    printf("Enter number of columns: ");
    scanf("%d", &cols);

    centerRow = (rows + 1) / 2;
    centerCol = (cols + 1) / 2;

    for(i=1; i<=rows; i++)
    {
        for(j=1; j<=cols; j++)
        {
            if(centerCol == j && centerRow == i)
            {
                printf("0");
            }
            else if(cols%2 == 0 && centerCol+1 == j)
            {
                if(centerRow == i || (rows%2 == 0 && centerRow+1 == i))
                    printf("0");
                else
                    printf("1");
            }
            else if(rows%2 == 0 && centerRow+1 == i)
            {
                if(centerCol == j || (cols%2 == 0 && centerCol+1 == j))
                    printf("0");
                else
                    printf("1");
            }
           else
            {
                printf("1");
            }
        }

        printf("\n");
    } 

    return 0;
}
Enter number of rows: 5                                                                                                                         
Enter number of columns: 5                                                                                                                      
11111                                                                                                                                           
11111                                                                                                                                           
11011                                                                                                                                           
11111                                                                                                                                           
11111                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.  

Number pattern 5
#include <stdio.h>

int main()
{
    int rows, cols, i, j, k;
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    printf("Enter number of columns: ");
    scanf("%d", &cols);

    k = 1;

    for(i=1; i<=rows; i++)
    {
        for(j=1; j<=cols; j++)
        {
            if(k == 1)
            {
                printf("1");
            }
            else
            {
                printf("0");
            }

            k *= -1;
        }

        if(cols % 2 == 0)
        {
            k *= -1;
        }

        printf("\n");
    }

    return 0;
}
Enter number of rows: 5                                                                                                                         
Enter number of columns: 5                                                                                                                      
10101                                                                                                                                           
01010                                                                                                                                           
10101                                                                                                                                           
01010                                                                                                                                           
10101                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.         

1.WAP to check a number is divisible by 5 and 11 or not.
#include <stdio.h>

int main()
{
    int num;
    printf("Enter any number: ");
    scanf("%d", &num);
    if((num%5==0) && (num%11== 0) )
{
        printf("Number is divisible by 5 and 11");
    }
    else
    {
        printf("Number is not divisible by 5 and 11");
    }


    return 0;
}
Enter any number: 55                                                    
Number is divisible by 5 and 11                                                                                                                 
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                                  

2.WAP to check whether a character is uppercase or lowercase alphabet.
#include <stdio.h>

int main()
{
    char ch;
    printf("Enter any character: ");
    scanf("%c", &ch);


    if(ch >= 'A' && ch <= 'Z')
    {
        printf("'%c' is uppercase alphabet.", ch);
    }
    else if(ch >= 'a' && ch <= 'z')
    {
        printf("'%c' is lowercase alphabet.", ch);
    }
    else
    {
        printf("'%c' is not an alphabet.", ch);
    }


    return 0;
}
Enter any character: s                                                                                                                          
's' is lowercase alphabet.                                                                                                                      
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.              

3.WAP to input week number and print week day.
#include <stdio.h>

int main()
{
    int week;
    printf("Enter week number (1-7): ");
    scanf("%d", &week);


    if(week == 1)
    {
        printf("Monday");
    }
    else if(week == 2)
    {
        printf("Tuesday");
    }
    else if(week == 3)
    {
        printf("Wednesday");
    }
    else if(week == 4)
    {
        printf("Thursday");
    }
    else if(week == 5)
    {
        printf("Friday");
    }
    else if(week == 6)
    {
        printf("Saturday");
    }
    else if(week == 7)
    {
        printf("Sunday");
    }
    else
    {
        printf("Invalid Input! Please enter week number between 1-7.");
    }

    return 0;
}
Enter week number (1-7): 5                                                                                                                      
Friday                                                                                                                                          
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.        

4.WAP to input month number and print number of days in that month.
#include <stdio.h>

int main()
{
    int month;
    printf("Enter month number (1-12): ");
    scanf("%d", &month);


    if(month == 1)
    {
        printf("31 days");
    }
    else if(month == 2)
    {
        printf("28 or 29 days");
    }
    else if(month == 3)
    {
        printf("31 days");
    }
    else if(month == 4)
    {
        printf("30 days");
    }
    else if(month == 5)
    {
        printf("31 days");
    }
    else if(month == 6)
    {
        printf("30 days");
    }
    else if(month == 7)
    {
        printf("31 days");
    }
    else if(month == 8)
    {
        printf("31 days");
    }
    else if(month == 9)
    {
        printf("30 days");
    }
    else if(month == 10)
    {
        printf("31 days");
    }
    else if(month == 11)
    {
        printf("30 days");
    }
    else if(month == 12)
    {
        printf("31 days");
    }
    else
    {
        printf("Invalid input! Please enter month number between (1-12).");
    }

    return 0;
}
Enter month number (1-12): 1                                                                                                                    
31 days                                                                                                                                         
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                                       

5.WAP to count total number of notes in a given amount.
#include <stdio.h>

int main()
{
    int amount;
	    
    int note1, note2, note5, note10, note20, note50, note100, note500;
    
    note1 = note2 = note5 = note10 = note20 = note50 = note100 = note500 = 0;     
    
    printf("Enter amount: ");
    scanf("%d", &amount); 
 
    if(amount >= 500)
    {
        note500 = amount/500;
        amount -= note500 * 500;
    }
    if(amount >= 100)
    {
        note100 = amount/100;
        amount -= note100 * 100;
    }
    if(amount >= 50)
    {
        note50 = amount/50;
        amount -= note50 * 50;
    }
    if(amount >= 20)
    {
        note20 = amount/20;
        amount -= note20 * 20;
    }
    if(amount >= 10)
    {
        note10 = amount/10;
        amount -= note10 * 10;
    }
    if(amount >= 5)
    {
        note5 = amount/5;
        amount -= note5 * 5;
    }
    if(amount >= 2)
    {
        note2 = amount /2;
        amount -= note2 * 2;
    }
    if(amount >= 1)
    {
        note1 = amount;
    }
 
    printf("Total number of notes = \n");
    printf("500 = %d\n", note500);
    printf("100 = %d\n", note100);
    printf("50 = %d\n", note50);
    printf("20 = %d\n", note20);
    printf("10 = %d\n", note10);
    printf("5 = %d\n", note5);
    printf("2 = %d\n", note2);
    printf("1 = %d\n", note1);

    return 0;
}
Enter amount: 500                                                                                                                               
Total number of notes =                                                                                                                         
500 = 1                                                                                                                                         
100 = 0                                                                                                                                         
50 = 0                                                                                                                                          
20 = 0                                                                                                                                          
10 = 0                                                                                                                                          
5 = 0                                                                                                                                           
2 = 0                                                                                                                                           
1 = 0                                                                                                                                           
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.  

6.WAP to input angles of a triangle and check whether triangle is valid or not.
#include <stdio.h>

int main()
{
     int a, b, c, sum;
    printf("Enter three angles of a triangle: ");
    scanf("%d %d %d", &a, &b, &c );
    sum = a+b+c;

    if (sum == 180)
        printf("Triangle is valid");
    else
        printf("Triangle is not valid");


    return 0;
}
Enter three angles of a triangle: 60                                                                                                            
60                                                                                                                                              
60                                                                                                                                              
Triangle is valid                                                                                                                               
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.                                                                                                                    
                              

7.WAP to input all sides of a triangle and check whether triangle is valid or not.
#include <stdio.h>

int main()
{
    int side1, side2, side3;
    printf("Enter three sides of triangle: \n");
    scanf("%d%d%d", &side1, &side2, &side3);
    
    if((side1 + side2) > side3)
    {
        if((side2 + side3) > side1)
        {
            if((side1 + side3) > side2) 
            {
                printf("Triangle is valid.");
            }
            else
            {
                printf("Triangle is not valid.");
            }
        }
        else
        {
            printf("Triangle is not valid.");
        }
    }

    return 0;
}
Enter three sides of triangle:                                                                                                                  
56                                                                                                                                              
23                                                                                                                                              
11                                                                                                                                              
Triangle is not valid.                                                                                                                          
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.  

8.WAP to check whether a triangle is equilateral , isosceles , or scalene triangle  .
#include <stdio.h>

int main()
{
    int side1, side2, side3;
 
  	printf("\n Enter Three Sides of a Triangle : ");
  	scanf("%d%d%d", &side1, &side2, &side3);
  	
  	if(side1 == side2 && side2 == side3)
  	{
  		printf("\n This is an Equilateral Triangle");
 	}
 	else if(side1 == side2 || side2 == side3 || side1 == side3)
 	{
 		printf("\n This is an Isosceles Triangle");
	}
	else
	{
		printf("\n This is a Scalene Triangle");
	}  

    return 0;
} Enter Three Sides of a Triangle : 10                                                                                                    
  Enter Three Sides of a Triangle : 10                                                                                                    
10                                                                                                                                              
10                                                                                                                                              
                                                                                                                                                
 This is an Equilateral Triangle                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.   

9.WAP to calculate profit or loss .
#include <stdio.h>

int main()
{
    int cp, sp;  
  
    printf("Enter the cost price of the product\n");  
    scanf("%d", &cp);  
  
    printf("Enter the selling price of the product\n");  
    scanf("%d", &sp);  
  
    if(sp > cp)  
    {  
        printf("Your profit is %d\n", (sp-cp));  
    }  
    else if(cp > sp)  
    {  
        printf("Loss is %d\n", (cp-sp));  
    }  
    else  
    {  
        printf("Neither profit, nor loss\n");  
    }  

    return 0;
}
Enter the cost price of the product                                                                                                             
50                                                                                                                                              
Enter the selling price of the product                                                                                                          
60                                                                                                                                              
Your profit is 10                                                                                                                               
                                                                                                                                                
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.   

10.WAP to input five subjects marks and calculate percentage and grade in physics , chemistry, biology , maths , computer .
#include <stdio.h>

int main()
{
    int phy, chem, bio, math, comp; 
    float per; 

    printf("Enter five subjects marks: ");
    scanf("%d%d%d%d%d", &phy, &chem, &bio, &math, &comp);

    per = (phy + chem + bio + math + comp) / 5.0;

    printf("Percentage = %f\n", per);

    if(per >= 90)
    {
        printf("Grade A");
    }
    else if(per >= 80)
    {
        printf("Grade B");
    }
    else if(per >= 70)
    {
        printf("Grade C");
    }
    else if(per >= 60)
    {
        printf("Grade D");
    }
    else if(per >= 40)
    {
        printf("Grade E");
    }
    else
    {
        printf("Grade F");
    }

    return 0;
}
Enter five subjects marks: 50                                                                                                                   
50                                                                                                                                              
50                                                                                                                                              
50                                                                                                                                              
50                                                                                                                                              
Percentage = 50.000000                                                                                                                          
Grade E                                                                                                                                         
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.           

11.WAP to input basic salary of an employee and calculate its gross salary .
#include <stdio.h>

int main()
{
    float basic, gross, da, hra;
    printf("Enter basic salary of an employee: ");
    scanf("%f", &basic);

    if(basic <= 10000)
    {
        da  = basic * 0.8;
        hra = basic * 0.2;
    }
    else if(basic <= 20000)
    {
        da  = basic * 0.9;
        hra = basic * 0.25;
    }
    else
    {
        da  = basic * 0.95;
        hra = basic * 0.3;
    }
    gross = basic + hra + da;

    printf("GROSS SALARY OF EMPLOYEE = %f", gross);

    return 0;
}
Enter basic salary of an employee: 50000                                                                                                        
GROSS SALARY OF EMPLOYEE = 112500.000000                                                                                                        
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.           

12.WAP to input electricity unit charges and calculate total electricity bill .
#include <stdio.h>

int main()
{
    int unit;
float amt, total_amt, sur_charge;
printf("Enter total consumed units: ");
scanf("%d", &unit);


if(unit <= 50)
{
amt = unit * 0.50;
}
else if(unit <= 150)
{
amt = 25 + ((unit-50)*0.75);
}
else if(unit <= 250)
{
amt = 100 + ((unit-150)*1.20);
}
else if(unit > 250)
{
amt = 220 + ((unit-250)*1.50);
}

sur_charge = amt*0.20;
total_amt = amt+sur_charge;

printf("\nElectricity Bill = Rs. %f", total_amt);


    return 0;
}
Enter total consumed units: 500                                                                                                                 
                                                                                                                                                
Electricity Bill = Rs. 714.000000                                                                                                               
                                                                                                                                                
...Program finished with exit code 0                                                                                                            
Press ENTER to exit console.       

