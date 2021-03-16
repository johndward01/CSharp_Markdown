 # Arrays & Lists
## Why: 
For many applications, you want to create and manage groups of related objects. There are two ways to group objects: by creating arrays of objects, and by creating collections of objects. Arrays are most useful for creating and working with a fixed number of strongly-typed objects. Collections provide a more flexible way to work with groups of objects. Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change. For some collections, you can assign a key to any object that you put into the collection so that you can quickly retrieve the object by using the key.

## What: 
A collection is a class, so you must declare an instance of the class before you can add elements to that collection. If your collection contains elements of only one data type, you can use one of the classes in the System.Collections.Generic namespace. A generic collection enforces type safety so that no other data type can be added to it. When you retrieve an element from a generic collection, you do not have to determine its data type or convert it.

## **Lists**

First we access the namespace needed to use Lists

```cs
using System;
using System.Collections.Generic; // We need this using directive

namespace Arrays_Collections
{
    class Program
    {
        static void Main(string[] args)
        {

        }
    }
}
```
Then we declare a List\<T>

Let's make a List of type int and name it "numbers"

```cs
static void Main(string[] args)
{
    var numbers = new List<int>();
}
```

Now we can add integers to the List using a "for" loop. With this setup, we'll add only even numbers up to 100 to our List. We do this by calling an **Add()** method

```cs
static void Main(string[] args)
{
    var numbers = new List<int>();

    for (int i = 0; i < 100; i+=2)
    {
        numbers.Add(i);
    }
}
```

Afterwards we can display our List to the console using a “foreach” loop, with Console.WriteLine() in the body: 

```cs
static void Main(string[] args)
{
    var numbers = new List<int>();

    for (int i = 0; i < 100; i+=2)
    {
        numbers.Add(i);
    }

    foreach(var num in numbers)
    {
        Console.WriteLine(num);
    }
}
```

Our List displays up to 98, because our conditional is set to "less than", not "less than or equal to"

## Arrays:

```cs
static void Main(stirng[] args)
{
    // Declare a single-dimensional array.
    int[] array1 = new int[5];

    // Declare and initialize a single-dimensional array.
    int[] array2 = new int[] { 1, 3, 5, 7, 9 };

    // Alternative syntax for declaring and initializing 
    int[] array3 = { 1, 2, 3, 4, 5, 6 };

    // Declare a two dimensional array.
    int[,] multiDimensionalArray1 = new int[2,3];

    // Declare and initialize a two dimensional array.
    int[,] multiDimensionalArray2 = { {1, 2, 3}, {4, 5, 6} };

    // Declare a jagged array.
    int[][] jaggedArray = new int[6][]; // an array of 6 single dimensional arrays

    // Set the values of the first array in the jagged array.
    jaggedArray[0] = new int[4] {1, 2, 3, 4 };

}
```

To use Arrays, we don’t have to use another namespace other than **using System;**

### How: 
Let’s take a look at our Banking Application. We can create collections of months to determine accounts that accumulate interest on a quarterly cycle. (This will become more advanced as the course continues).

We can use an array since there are a fixed number of Months in every year: 

```cs
string[] months = {"Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"};
```

Then by using a for loop with a nested if statement, we can determine if the month at index “i” is equal to the current month, we want to call our **AddInterest()** method from our Banking Application example.

```cs
for (int i = 0; i < months.Length; i++)
{
    if (months[i] == currentMonth)
    {
        Console.WriteLine(prog.AddInterest(balance, currentInterest));
    }
}
```

## Exercise 1: 
Clone the following repository: https://github.com/mvdoyle/ArrayAndListQuiz
**Do not fork**

Run the application once cloned and answer the questions in the terminal/command prompt
See if you can improve your score!

---------

## Exercise 2: 
Video: https://vimeo.com/453366989/5dd156eac3

First, fork the repository from https://github.com/mvdoyle/ArraysAndListsProject
Then, clone the repo onto your personal machine and follow the instructions in the Project. 
When finished, push your project back up to GitHub and mark the assignment as complete in Google Classroom. 

-------

## Exercise 3: 
Videos: 
- Part 1: Arrays https://vimeo.com/453367398/ac818e71de
- Part 2: Lists https://vimeo.com/453418510/8d8a69a6ce

Fork the repository from https://github.com/mvdoyle/CollectionsMasterApp
Then, clone the repo onto your personal machine and follow the instructions in the Project. 

------


### Quiz: 
https://docs.google.com/forms/d/1okEnXJK3PTmM2CRPZQIlVPhglfk_jynfSEF_OXt86-w/edit 

Tutorial: https://docs.microsoft.com/en-us/dotnet/csharp/tutorials/intro-to-csharp/list-collection