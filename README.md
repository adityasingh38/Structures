
# Structures

In C, structures are a way to group together variables of different types under a single name. A structure is defined using the 'struct' keyword, followed by the name of the structure and the variables that it contains.

![structure_memory_allocation](https://user-images.githubusercontent.com/88421625/234413217-aca263b1-c0a7-4f33-8877-6a40094ac519.png)


Here is an example of defining a structure in C:

```
struct person {
  char name[50];
  int age;
  float height;
};
```
In this example, we define a structure called 'person' that contains three variables: a string called 'name', an integer called 'age', and a float called 'height'.

You can then declare variables of the 'person' type and initialize them like this:
```
struct person john = {"John Doe", 30, 1.75};
```
In this example, we declare a variable called 'john' of the 'person' type and initialize its 'name', 'age', and 'height' fields.

You can access individual fields of a structure using the dot notation, like this:
```
printf("Name: %s\n", john.name);
printf("Age: %d\n", john.age);
printf("Height: %f\n", john.height);
```
In this example, we access the fields of the 'john' structure using the pointer 'pJohn'.

Structures in C are often used to represent complex data structures, such as linked lists, trees, and graphs.
## Key Points
Here are some important points about Structures:

•	Structures are defined using the struct keyword, followed by the name of the structure and the variables that it contains.

•	You can declare variables of the structure type and initialize them using curly braces {}.

•	You can access individual fields of a structure using the dot notation . to access fields of a structure variable or using the arrow notation -> when accessing fields of a structure through a pointer to a structure variable.

•	Structures can be nested within other structures.

•	Structures in C are passed to functions by value, meaning that a copy of the structure is made when passed to a function. However, you can also pass a pointer to a structure to modify the original structure.

•	Structures can be used to represent complex data structures such as linked lists, trees, and graphs.

•	You can define a structure with a typedef to make it easier to declare variables of the structure type.

•	Structures can have flexible array members at the end, which allows you to create structures with variable-length arrays.

•	Structures can be used with unions to create a single variable that can hold multiple data types.

# Code

```bash
// A. creating a database of vehicles by storing information like:
// 1. name
// 2. manufacturing year
// 3. cost
// 4. category (high end (H) / middle (M) / low end (L))
// make a structure to store the above information about a vehicle.



#include <stdio.h>

// creating a structure and naming it 'car'
struct car
{
	char name[50];
	int mYear;
	int cost;
	char category;
};

struct car model[3];

int main()
{
	// int i, j;
	
	// declaring an array of the struct data type 'car' and calling it 'model'
	
	// taking user input for the name, manufacturing year, cost and category
	//printf("Name: ");
	//scanf("%s", &model.name);
	
	//printf("Manufacturing Year: ");
	//scanf("%d", &model.mYear);
	
	//printf("Cost: ");
	//scanf("%d", &model.cost);
	
	//printf("%s %d %d", model.name, model.mYear, model.cost);
	
	
	/*
	// storing details of 10 (3 for now) cars in an array
	for(i = 0; i < 3; i++)
	{
		printf("Name: ");
		scanf("%s", &model[i].name);
	
		printf("Manufacturing Year: ");
		scanf("%d", &model[i].mYear);
		
		printf("Cost: ");
		scanf("%d", &model[i].cost);		
		
		printf("\n\n\n");
	}
	
	
	printf("Available Database: \n\n");
	printf("Name  MYear  Cost \n");
	
	for(j = 0; j < 3; j++)
	{
		printf("%s  %d  %d \n", model[j].name, model[j].mYear, model[j].cost);
	}
	*/
	
	userInput();
	printInput();
	
	return 0;
}



// B. make two functions: one takes user input, the other prints it

void userInput()
{
	int i;
	
	// storing details of 10 (3 for now) cars in an array
	for(i = 0; i < 3; i++)
	{
		printf("Name: ");
		scanf("%s", &model[i].name);
	
		printf("Manufacturing Year: ");
		scanf("%d", &model[i].mYear);
		
		printf("Cost: ");
		scanf("%d", &model[i].cost);		
		
		printf("\n\n\n");
	}
		
}

void printInput()
{
	int j;
	
	printf("Available Database: \n\n");
	printf("Name  MYear  Cost \n");
	
	for(j = 0; j < 3; j++)
	{
		printf("%s  %d  %d \n", model[j].name, model[j].mYear, model[j].cost);
	}
	
}
```
## Output

![Screenshot 2023-04-26 032407](https://user-images.githubusercontent.com/88421625/234412983-66063bc6-92e8-4fbb-8c9b-a1bf653fa5a0.png)
