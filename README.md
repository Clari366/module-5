# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>
int main()
{
int mlenght,width
int*len=len&lenght, *wid=&width;
scanf("%d%d",len,wid);
float area=(*len)*(*wid);
printf("Area of rectangle = %f sq. units ", area);
return 0;
}
```
## OUTPUT
		       	
![438209239-9cb2e583-562c-4871-8838-70aec142acee](https://github.com/user-attachments/assets/b71e26d1-c6fe-4afb-b5e9-d5eb2bfafc67)


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include<stdio.h>
#include<stdlib.h>
int main()
{
char *str = (char *)malloc(8 * size(char));
if (str == NULL)
{
printf("Memory allocation failed!\n);
return 1;
}
str[0] = 'w'
str[1] = 'E';
str[2] ='L'
str[3] ='C'
str[4[ ='O'
str [5] ='M'
str[6] ='E'
str[7] ='\0';
printf("%s\n",str);
free(str);
return 0;
}
```
## OUTPUT

![438209832-f4c3ccc1-18ee-4cd4-afb6-91d8d4dfb242](https://github.com/user-attachments/assets/b9a70fa1-450c-4122-94c6-4b75ad75f6b3)


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct Employee 
{
    int id;
    char name[50];
    float age;
};

int main() 
{
    struct Employee employees;
    scanf("%d", &employees.id);
    scanf(" %s", employees.name);
    scanf("%f", &employees.age);
    printf("Rollno is: %d\nName is: %s\nPercentage is: %.2f\n", employees.id, employees.name, employees.age);
  

    return 0;
}
```

## OUTPUT

![438200725-c3d1db83-f99e-4dbc-a476-ffae39c1049e](https://github.com/user-attachments/assets/7e06f61b-b47b-45a7-902f-39797bf8794e)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>
struct employee
{
int eno;
char dept[20];
float basicpay;
float da;
float hra;
float grossSalary;
};
int main()
{
struct employee emp[3]
for (int i=0;i<3;i++)
{
scanf("%d %s %f", &emp[i].eno,emp[i].dept,&emp[i].basipay);
emp[i].da=emp[i].basicpay*0.10;
emp[i].hra=emp[i].basicpay*0.30;
emp[i].grossSalary=emp[i].basicpay+emp[i].hra;
}
printf("Details of the Employee:\n);
for(int i=0;,i<3;i++)
{
printf("%d %s %.0f %.0f %.2f\n", emp[i].eno,emp[i].dept,emp[i].basicpay,em
}
}
```

 ## OUTPUT
 
![438210760-457d0649-b2d2-4eca-9cde-64a0fcc3bf3c](https://github.com/user-attachments/assets/8d99c40b-2e43-4d06-9ce0-468a108456c5)

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

struct Student {
    char name[50];
    int marks[5];
    float total;
    float average;
};

int main() {
    struct Student student;
    int sum = 0;

    printf("Enter student's name: ");
    scanf("%s", student.name);

    printf("Enter marks for 5 subjects:\n");
    for (int i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%d", &student.marks[i]);
        sum += student.marks[i];
    }

    student.total = sum;
    student.average = sum / 5.0;

    printf("\nStudent Name: %s\n", student.name);
    printf("Total Marks: %.2f\n", student.total);
    printf("Average Marks: %.2f\n", student.average);

    return 0;
}
```

## OUTPUT

 ![Screenshot 2025-05-30 095253](https://github.com/user-attachments/assets/5c2b73d2-29b6-4f96-9f1d-e6826668b327)



## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


