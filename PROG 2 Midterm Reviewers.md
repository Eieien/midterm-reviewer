# Loyalty Award
![[Pasted image 20250309113310.png]]
#### Sample output 1: 
```
Input Number of Employees:3

Input Details for Employees:


===Employee 1===
Input First Name: Patrick
Input Month of Hire: 08
Input Year of Hire: 2018


===Employee 2===
Input First Name: Ean
Input Month of Hire: 07
Input Year of Hire: 2018


===Employee 3===
Input First Name: Gran
Input Month of Hire: 12
Input Year of Hire: 2017
Loyal List:

Name: Ean -- Hire Date:7-2018
Name: Gran -- Hire Date:12-2017
```
#### Sample Output 2:
```
Input Number of Employees:2

Input Details for Employees:


===Employee 1===
Input First Name: Josh
Input Month of Hire: 08
Input Year of Hire: 2018


===Employee 2===
Input First Name: John
Input Month of Hire: 09
Input Year of Hire: 2017
Loyal List:

Name: John -- Hire Date:9-2017
```
#### Sample Output 3:
```
Input Number of Employees:3

Input Details for Employees:


===Employee 1===
Input First Name: Justin
Input Month of Hire: 08
Input Year of Hire: 2018


===Employee 2===
Input First Name: Dave
Input Month of Hire: 09
Input Year of Hire: 2020


===Employee 3===
Input First Name: Chris
Input Month of Hire: 10
Input Year of Hire: 2019
There are currently no Employees who are eligible for the reward.
```

# Non-ADT Game Time
![[Pasted image 20250309113546.png]]
#### Sample Output 1:
```
Choose Which Items to Use:
1. Highest Attack
2. Highest Defense
Input Choice: 1


Current Equipment:
Helmet : Rune Helmet
Armor : Light Armor
Weapon : Silver Sword

Current Stats:
Player Atk: 679
Player Def: 183
```
#### Sample Output 2:
```
Choose Which Items to Use:
1. Highest Attack
2. Highest Defense
Input Choice: 2


Current Equipment:
Helmet : Leather Helmet
Armor : Silver Armor
Weapon : Gold Spear

Current Stats:
Player Atk: 432
Player Def: 523
```

# True or False
![[Pasted image 20250309113717.png]]
#### Sample Output 1:
```
How many students in the class? 2
===STUDENT 1===

Input First Name: Patrick
Input Last Name: Elalto
Input Middle Initial: C
Input Students Answer [10]: TTFTFFFTTF
===STUDENT 2===

Input First Name: Ean
Input Last Name: Velayo
Input Middle Initial: C
Input Students Answer [10]: FFTTFFTTFF

===STUDENT 1===

Student Name: Elalto, Patrick 
Student Answer: TTFTFFFTTF
Student Score: 5 / 10



===STUDENT 2===

Student Name: Velayo, Ean 
Student Answer: FFTTFFTTFF
Student Score: 4 / 10
```
#### Sample Output 2:
```
How many students in the class? 0
Class Count has to be greater than 0
```
#### Sample Output 3:
```
ow many students in the class? 3
===STUDENT 1===

Input First Name: Gorii
Input Last Name: Guanzon
Input Middle Initial: D
Input Students Answer [10]: TTTTTTTTTT
===STUDENT 2===

Input First Name: Jason
Input Last Name: Vero
Input Middle Initial: B
Input Students Answer [10]: FFFFFFFFFF
===STUDENT 3===

Input First Name: NJ
Input Last Name: Ompad
Input Middle Initial: B
Input Students Answer [10]: TTTFFTTFTF

===STUDENT 1===

Student Name: Guanzon, Gorii 
Student Answer: TTTTTTTTTT
Student Score: 6 / 10



===STUDENT 2===

Student Name: Vero, Jason 
Student Answer: FFFFFFFFFF
Student Score: 4 / 10



===STUDENT 3===

Student Name: Ompad, NJ 
Student Answer: TTTFFTTFTF
Student Score: 10 / 10
```

#### Required Files
##### display.h
```
#ifndef DISPLAY_H
#define DISPLAY_H
#define MAX 10

typedef struct{
    char fName[50];
    char lName[50];
    char MI;
}name;

typedef struct{
    name studentName;
    char studentAnswer[MAX];
    int studentScore;
}studentResults;

typedef struct{
    studentResults *record;
    int count;
}classRecord;

void display(classRecord);
studentResults addStudent(char[],char[],char,char[]);

#endif
```
##### main.c
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>
#include "display.h"

code here...
```
# Adventures of Mr. Pointy and Friends
![[Pasted image 20250309113846.png]]
#### Sample Output 1:
```
Enter x - coordinate: 0
Enter y - coordinate: 0
Mr Pointy (0, 0) is in Origin.
Friends: {(0, 0)}
```
#### Sample Output 2:
```
Enter x - coordinate: 5
Enter y - coordinate: 7
Mr Pointy (5, 7) is in Q1.
Friends: {(6, 9), (7, 11), (4, 7), (1, 12)}
```

#### Sample Output 3:
```Enter x - coordinate: 0
Enter y - coordinate: -7
Mr Pointy (0, -7) is in y-axis.
Friends: {(0, 10), (0, -3), (0, -10)}
```
#### Required files:
##### pointy.h
```
#ifndef POINTY_H
#define POINTY_H

typedef char String[20];

typedef struct {
    int x, y;
} MyPoint;

typedef struct {
    MyPoint *points;
    int count;
    int max;
} Points;

/**
    The function displayPoint() will accept MyPoint and display the x and y coordinates.
*/
void displayPoint(MyPoint p);

/**
    The function displayPointMsg() will accept a MyPoint and will display the x and y coordinates with the location and position.
*/
void displayPointMsg(MyPoint p);

/**
    The function identifyPoint() will determine the location of the given point base in the cartesian plane.
*/
int identifyPoint(MyPoint p);

/**
    The function createPoint() will make a MyPoint based from the x and y coordinate.
*/
MyPoint createPoint(int x, int y);

/**
    Initialize a structure of a collection of points (dynamically allocated) based on the max value.
*/
void initPoints(Points *p, int max);

/**
    Initialize a structure of a collection of points (statically allocated) based on the max value of 30.
*/
Points createPoints();

/**
    The function displayAllPointsWithStartIndex() will display the points in the collection from the "start" value until to the end.
*/
void displayAllPointsWithStartIndex(Points p, int start);

//Points getMrPointyAndFriends(Points points);

/**
    Populates with initial point values values in "p".
*/
void populatePoints(Points *p);

#endif
```
##### originalFile.c
```
// #include <stdio.h>
// #include <stdlib.h>
// #include "pointy.h"

// Points getMrPointyAndFriends(Points points) {
//     // to do code login here

// }

// void main() {
//     Points points = createPoints(30);
//     Points friends;
//     int x, y;

//     populatePoints(&points);

//     printf("Enter x - coordinate: ");
//     scanf("%d", &x);
//     printf("Enter y - coordinate: ");
//     scanf("%d", &y);

//     // insert code to override the first value in the populated
//     // points by the new value x and y after this comment

//     displayPointMsg(points.points[0]);
//     printf("Friends: ");
//     // insert you function call of getMrPointyAndFriends()

//     displayAllPointsWithStartIndex(friends, 1);
// }
```

##### main.c
```
#include <stdio.h>
#include <stdlib.h>
#include "pointy.h"

/**
    Function: getMrPointyAndFriends()
    Description: The function will get all points with the same cluster (location) in the cartesian plane. Mr Pointy is the first index in the collection followed by the others.
    Param: points - a collection of points starting with Mr. Pointy followed by the others.
    Return: a collection of Mr Pointy and with his friends. Still Mr Pointy will still be in the first index follwed by his friends.
*/
```

# What's the POINT?
![[Pasted image 20250309114026.png]]
![[Pasted image 20250309114056.png]]
![[Pasted image 20250309114041.png]]
#### Sample Output 1:
```
Enter x - coordinate: 0
Enter y - coordinate: 0
The point (0, 0) is in Origin.
```
#### Sample Output 2:
```
Enter x - coordinate: 5
Enter y - coordinate: 4
The point (5, 4) is in Q1.
```
#### Sample Output 3:
```
Enter x - coordinate: -4
Enter y - coordinate: 7
The point (-4, 7) is in Q2.
```

# Structure Me
![[Pasted image 20250309114213.png]]
#### Sample Output 1:
```
4 - Marshmallows - Php 150.00
5 - Netflix Giftcard - Php 500.00
7 - Alarm Clock - Php 1500.00
8 - Backpack - Php 1000.00
10 - Self-Help Book - Php 300.00
```

# Exam Checking
![[Pasted image 20250309114306.png]]
#### Sample Output 1:
```
Input Number of Students in Class:4
===STUDENT 1===

Input First Name: Patrick
Input Last Name: Elalto
Input Middle Initial: M
Input ID Number: 13100270
Input Exam Score 1: 80
Input Exam Score 2: 70
Input Exam Score 3: 60
===STUDENT 2===

Input First Name: Gran
Input Last Name: Sabandal
Input Middle Initial: G
Input ID Number: 21068332
Input Exam Score 1: 95
Input Exam Score 2: 65
Input Exam Score 3: 80
===STUDENT 3===

Input First Name: Erwin
Input Last Name: Sarmiento
Input Middle Initial: E
Input ID Number: 205343125
Input Exam Score 1: 59
Input Exam Score 2: 90
Input Exam Score 3: 43
===STUDENT 4===

Input First Name: Ean
Input Last Name: Velayo
Input Middle Initial: S
Input ID Number: 13100271
Input Exam Score 1: 55
Input Exam Score 2: 51
Input Exam Score 3: 60
Retakers Needed for Exam 1:Erwin Ean

Retakers Needed for Exam 2:Ean

Retakers Needed for Exam 3:Erwin
```
#### Sample Output 2:
```
Input Number of Students in Class:11
Maximum Number of Students per Class is only 10
```
#### Sample Output 3:
```
Input Number of Students in Class:2
===STUDENT 1===

Input First Name: Tim
Input Last Name: Boone
Input Middle Initial: A
Input ID Number: 210534613
Input Exam Score 1: 50
Input Exam Score 2: 80
Input Exam Score 3: 90
===STUDENT 2===

Input First Name: Remi
Input Last Name: Warner
Input Middle Initial: K
Input ID Number: 2053624362
Input Exam Score 1: 57
Input Exam Score 2: 66
Input Exam Score 3: 83
Retakers Needed for Exam 1:All Students Have to Retake Exam 1

Retakers Needed for Exam 2:No Retakers for Exam 2

Retakers Needed for Exam 3:No Retakers for Exam 3
```

# Structures Practice ll
![[Pasted image 20250309114405.png]]
#### Sample Output 1:
```
Enter radius: 5
Circumference: 31.42
Area: 78.54
```
#### Sample Output 2:
```
Enter radius: 8
Circumference: 50.27
Area: 201.06
```
#### Sample Output 3:
```
Enter radius: 10
Circumference: 62.83
Area: 314.16
```
# Store Necessities
![[Pasted image 20250309114511.png]]
![[Pasted image 20250309114516.png]]
![[Pasted image 20250309114528.png]]
![[Pasted image 20250309114537.png]]
![[Pasted image 20250309114544.png]]
#### Sample Output 1:
```
Input Current Month: 3
Input Current Year: 2024


=====ITEMS LIST======
PRODUCT NAME               UNIT PRICE            QUANTITY         EXPIRY DATE
------------               ----------            --------         -----------

Milk                           100.00                   8              3/2024
Chicken                        250.00                   4              7/2024
Oil                            80.50                    4             10/2024
Beef                           230.75                   3              3/2024
Pork                           200.50                   5              2/2024
Ketchup                        110.85                   8              6/2024
Soda                           89.50                   10              9/2024
Beer                           120.00                  10              1/2025
Bottled Water                  50.00                   30              2/2025
Salad Dressing                 125.50                   9              3/2024


Inventory Value: 9428.05


=====ITEM LIST AFTER EXPIRED REMOVAL======
PRODUCT NAME               UNIT PRICE            QUANTITY         EXPIRY DATE
------------               ----------            --------         -----------

Chicken                        250.00                   4              7/2024
Oil                            80.50                    4             10/2024
Ketchup                        110.85                   8              6/2024
Soda                           89.50                   10              9/2024
Beer                           120.00                  10              1/2025
Bottled Water                  50.00                   30              2/2025


Inventory Value: 5803.80


=====ITEMS IN EXPIRED LIST======
PRODUCT NAME               UNIT PRICE            QUANTITY         EXPIRY DATE
------------               ----------            --------         -----------

Milk                           100.00                   8              3/2024
Beef                           230.75                   3              3/2024
Pork                           200.50                   5              2/2024
Salad Dressing                 125.50                   9              3/2024


Loss Value: 3624.25
```
#### Sample Output 2:
```
Input Current Month: 1
Input Current Year: 2023


=====ITEMS LIST======
PRODUCT NAME               UNIT PRICE            QUANTITY         EXPIRY DATE
------------               ----------            --------         -----------

Milk                           100.00                   8              3/2024
Chicken                        250.00                   4              7/2024
Oil                            80.50                    4             10/2024
Beef                           230.75                   3              3/2024
Pork                           200.50                   5              2/2024
Ketchup                        110.85                   8              6/2024
Soda                           89.50                   10              9/2024
Beer                           120.00                  10              1/2025
Bottled Water                  50.00                   30              2/2025
Salad Dressing                 125.50                   9              3/2024


Inventory Value: 9428.05




No Currently Expired Items
```
#### Sample Output 3:
```
Input Current Month: 9
Input Current Year: 2024


=====ITEMS LIST======
PRODUCT NAME               UNIT PRICE            QUANTITY         EXPIRY DATE
------------               ----------            --------         -----------

Milk                           100.00                   8              3/2024
Chicken                        250.00                   4              7/2024
Oil                            80.50                    4             10/2024
Beef                           230.75                   3              3/2024
Pork                           200.50                   5              2/2024
Ketchup                        110.85                   8              6/2024
Soda                           89.50                   10              9/2024
Beer                           120.00                  10              1/2025
Bottled Water                  50.00                   30              2/2025
Salad Dressing                 125.50                   9              3/2024


Inventory Value: 9428.05


=====ITEM LIST AFTER EXPIRED REMOVAL======
PRODUCT NAME               UNIT PRICE            QUANTITY         EXPIRY DATE
------------               ----------            --------         -----------

Oil                            80.50                    4             10/2024
Beer                           120.00                  10              1/2025
Bottled Water                  50.00                   30              2/2025


Inventory Value: 3022.00


=====ITEMS IN EXPIRED LIST======
PRODUCT NAME               UNIT PRICE            QUANTITY         EXPIRY DATE
------------               ----------            --------         -----------

Milk                           100.00                   8              3/2024
Chicken                        250.00                   4              7/2024
Beef                           230.75                   3              3/2024
Pork                           200.50                   5              2/2024
Ketchup                        110.85                   8              6/2024
Soda                           89.50                   10              9/2024
Salad Dressing                 125.50                   9              3/2024


Loss Value: 6406.05
```

#### Required files
##### main.h
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "functions.h"
#include "problem.h"

int main(){
storeInventory store;
date currentDate;
store.expiredInventory.inventoryCount=0;
store.expiredInventory.inventoryCost=0;

printf("Input Current Month: ");
scanf("%d",&currentDate.month);
printf("Input Current Year: ");
scanf("%d",&currentDate.year);

addInitialInventory(&store.currentInventory);

display(store,1);

expiredProductRemoval(&store,currentDate);

display(store,2);

}
```

##### functions.h
```
#ifndef FUNCTIONS_H
#define FUNCTIONS_H


typedef struct{
int month;
int year;
}date;

typedef struct{
char productName[50];
float price;
date expiryDate;
int quantity;
}productInfo;

typedef struct{
productInfo *product;
float inventoryCost;
int inventoryCount;
}inventory;

typedef struct{
inventory currentInventory;
inventory expiredInventory;
}storeInventory;


void addInitialInventory(inventory*);
productInfo addProductInfo(char[],float,date,int);
date addDate(int,int);
void display(storeInventory,int);

#endif
```

##### problem.h
```
#ifndef PROBLEM_H
#define PROBLEM_H
#include "functions.h"

void expiredProductRemoval(/*Appropriate Parameters*/);

#endif
```

#### problem.c
```
Answer here...
```

# Esports Dilemma
![[Pasted image 20250309114917.png]]
![[Pasted image 20250309114924.png]]
#### Sample Output 1:
```
===Find Teams!===
Input School: SAS
Input Sport: LoL


=====SAS's LoL Team=====
Member 1: Mohammed, Jast -- Challenger
Member 2: Roberto, Schmitt -- Challenger
Member 3: Creola, Lehner -- Master
Member 4: Angus, Auer -- Emerald
Member 5: Emmanuelle, Bergnaum -- Diamond
Member 6: Carley, Blanda -- Platinum
```
#### Sample Output 2:
```
===Find Teams!===
Input School: SAS
Input Sport: Valorant


=====SAS's Valorant Team=====
Member 1: Eulah, Lynch -- Challenger
Member 2: Sandrine, Bergstrom -- Emerald
Member 3: Jody, MacGyver -- Gold
Member 4: Bennett, Schimmel -- Silver
Member 5: Jeremy, Robel -- Bronze
```
#### Sample Output 3:
```
===Find Teams!===
Input School: SOE
Input Sport: LoL


SOE does not have enough members in team to participate in LoL
```

#### Required Files
```
#ifndef FUNCTIONS_H_INCLUDED
#define FUNCTIONS_H_INCLUDED

typedef struct{
	char fname[20];
	char lname[20];
}name;

typedef struct{
	char esport[30];
	int rank;
}sportInfo;

typedef struct{
	name studentName;
	sportInfo game;
	char school[20]; //SOE,SAS,SAFAD
}studentInfo;

typedef struct{
	studentInfo *schoolList;
	int schoolCount;
}schoolList;

typedef struct{
	studentInfo *teamMembers; // Players have to reach a minimum of 5 to join, while a maximum of 6.
							  //Team Composition is based soley on Rank, the highest ranked of a department and game will
							  //be added to the team.
	char game[20];
	char teamDepartment[20];
	int count;
}team;

/* addStudent creates a studentInfo structure and populates it using the given arguments after which the studentInfo structure is returned back to calling function.*/

studentInfo addStudent(name studentName,sportInfo game,char school[]);


/* addName creates a name structure and populates it using the given arguments after which the name structure is returned back to calling function*/

name addName(char fname[20],char lname[20]);

/* sportInfo creates a name structure and populates it using the given arguments after which the sportInfo structure is returned back to calling function. You might notice that here rank is char[] but in the structure it is int, this function is passed a String equivalent of the rank such as "Gold", and the function converts that String counterpart to its equivalent integer value (e.g Gold gets converted to 3) */

sportInfo addSport(char game[20],char rank[20]);


/* populateSchoolList creates a list of all students who are interested in joining the tournament, this populates the necessary fields such as the players name, game of choice, rank, and department */

void populateSchoolList(schoolList *totalList);

/* display aims to display the output in the proper format */

void display(team foundTeam);

#endif
```

##### main.c
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "functions.h"

/* The functions available are found in .h, although these functions are available does not mean,
they are needed to be used in the actual solution. Most functions are used during the initial population of the list and can be ignored, but again are available if you see fit. */

/* display() and populateSchoolList() is really the only required function you need to call in the actual solution */

Code here...

```

# Tax Brackets
![[Pasted image 20250309115502.png]]
![[Pasted image 20250309115515.png]]
![[Pasted image 20250309115524.png]]
![[Pasted image 20250309115531.png]]
#### Sample Output 1:
```
Input how many employees: 1


===EMPLOYEE 1===

Input First Name: Patrick
Input Last Name: Elalto
Input Middle Initial: M
Input Id Number: 13100270
Input Rate: 1000
Input Hours Worked: 40

===============



===BRACKET 3===
13100270 - Elalto,Patrick M --- Php 32000.00
```
#### Sample Output 2:
```
Input how many employees: 3


===EMPLOYEE 1===

Input First Name: Jovan
Input Last Name: Aligway
Input Middle Initial: G
Input Id Number: 113842
Input Rate: 500
Input Hours Worked: 30


===EMPLOYEE 2===

Input First Name: Jimothy
Input Last Name: Garcia
Input Middle Initial: D
Input Id Number: 188324
Input Rate: 700
Input Hours Worked: 25


===EMPLOYEE 3===

Input First Name: Manolo
Input Last Name: Calatrava
Input Middle Initial: B
Input Id Number: 152334
Input Rate: 900
Input Hours Worked: 40

===============



===BRACKET 2===
113842 - Aligway,Jovan G --- Php 12750.00
188324 - Garcia,Jimothy D --- Php 14875.00


===BRACKET 3===
152334 - Calatrava,Manolo B --- Php 28800.00
```
#### Sample Output 3:
```
Input how many employees: 4


===EMPLOYEE 1===

Input First Name: Patrick
Input Last Name: Elalto
Input Middle Initial: M
Input Id Number: 131000
Input Rate: 1000
Input Hours Worked: 34


===EMPLOYEE 2===

Input First Name: Ean
Input Last Name: Velayo
Input Middle Initial: C
Input Id Number: 131100
Input Rate: 800
Input Hours Worked: 40


===EMPLOYEE 3===

Input First Name: Gran
Input Last Name: Sabandal
Input Middle Initial: G
Input Id Number: 133200
Input Rate: 300
Input Hours Worked: 40


===EMPLOYEE 4===

Input First Name: Chris
Input Last Name: Belarmino
Input Middle Initial: J
Input Id Number: 134110
Input Rate: 650
Input Hours Worked: 35

===============



===BRACKET 1===
133200 - Sabandal,Gran G --- Php 10800.00


===BRACKET 2===
134110 - Belarmino,Chris J --- Php 19337.50


===BRACKET 3===
131000 - Elalto,Patrick M --- Php 27200.00
131100 - Velayo,Ean C --- Php 25600.00
```

#### Required Files:
##### display.h
```
#ifndef DISPLAY_H_INCLUDED
#define DISPLAY_H_INCLUDED

typedef struct{
    char fName[20];
    char lName[20];
    char MI;
}name;

typedef struct{
    name empName;
    int idNum;
    int grossSalary;
    int rate;
    int hrsWorked;
    float takeHomeSalary;
}employeeInfo;

typedef struct{
    employeeInfo *employees;
    //employeeInfo employees[MAX]; //Can use statically allocated array instead of above.
    // Do note only efficiently allocated arrays will be given full marks. e.g: An array that will contain 5 items, should only be allocated memory to accomodate those 5 items.
    int count;
}employeeRecord;

typedef struct{
    employeeRecord employeeList;
    employeeRecord bracket1; //Transfer all Employees who earn a grossSalary of 0-14,999, Tax rate = 10%, calculate takeHomeSalary here
    employeeRecord bracket2; //Transfer all Employees who earn a grossSalary of 15,000-25,999, Tax rate = 15%, calculate takeHomeSalary here
    employeeRecord bracket3; //Transfer all Employees who earn a grossSalary of 26,000 or higher, Tax rate = 20%, calculate takeHomeSalary here
}companyRecord;

void display(companyRecord);
employeeRecord populate(int);
employeeInfo newEmployee(int,int,int,name);
name addName(char [],char[],char);
void taxBracketSeparation(companyRecord *);

#endif
```

##### main.c
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "display.h"

code here:
```