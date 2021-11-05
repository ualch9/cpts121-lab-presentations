A struct is essentially a Data Structure. Structuring your data simplifies how you (the programmer) processes data.

For example, if you recall in a previous PA,
```c
int student1ID;
char* student1Name;
int student1Age;
double student1GPA;
```

If you wanted to process another student, you would have to write an additional four lines of code,
```c
int student2ID;
char* student2Name;
int student2Age;
double student2GPA;
```

This becomes extremely messy, very quickly, as you have to deal with 4 extra variables for each student.

Instead, since the 4 variables are related to each other, we can put it into a Data Structure,
```c
typedef struct student {
    int id;
    char* name;
    int age;
    double gpa;
} Student;
```

Now, we can cut down the number of lines of code,
```c
Student student1;
Student student2;
```

If we wanted to access `student1`’s name, we would use `student1.name`.

This comes with the added benefit if we want an array of students,
```c
Student students[32];	// Declare an array of 32 students.
```
