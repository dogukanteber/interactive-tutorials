Tutorial
--------

An array in C is a collection of items stored at contiguous memory locations and elements can be accessed randomly using indices of an array. They are used to hold primitive data types such as int, float, char etc.

Since an array can hold only one data type values before declaring an array, we must specify what data types the array will hold, what will be the name of the array and what is the size. Follow the below blueprint when declaring an array:

`type name[size];`

If you understand what I have talked about above, let us create an integer array with size 20:

`int first_array[20];`

Wuhu. That is it. Easy peasy. Now, let us create an array with data inside:

`float grades[5] = { 78.6 , 65,2 , 98.0, 45.8, 87.4 };`

Above, we have created an array with size 5 and put some values in it. This is another way of declaring an array. We can put values inside when we first created the array. The cool part is when we put values inside the array, we do not need to give its size. The size will automatically arranged. Let us try to run the code in below:

`float grades[] = { 78.6 , 65,2 , 98.0, 45.8, 87.4 };`

Go ahead and try to run 3 types of arrays in your development environment(do not forget to include necessary libraries and the main function).

We have learned to declare an array but how do we put values inside it? There is one way of putting values inside but this may not be the situation every time. We do not have the luxury to put values as soon as we declare the array. Luckily, there is another way of putting values inside an array, called indexing. When you want to access a specific array just type its name and which value you want to access. But be careful, in indexing, counting starts from 0. So, first element in an array will be in 0th index. 

Array elements are accessed by using an integer index. Array index starts with 0 and goes till size of array minus 1.  0th index is pointing to 1, 1st index is pointing to 2 etc. For assigning values to specific indexes is done by equality operator.

Let us put everything we learned together. Take a look at the below program:

`
#include <stdio.h>
int main() {
  // declare the array and initialize elements 
  int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
  printf("%s", "Before change:\n");
  printf("First element : %d\nSecond element : %d", arr[0],arr[1]);
  // change the first and second element in the array
  arr[0] = 20;
  arr[1] = 30;
  // print out the values to be sure the values have changed
  printf("%s", "After change:\n");
  printf("First element : %d\nSecond element : %d", arr[0],arr[1]);
  return 0;
}
`

Above, we have declared and initialized our array. Then, we changed their values. Before and after the operations, we printed out the values.

Before finishing this article, I want to teach you a cool way to get user input into an array. Say, we have 10 people and our mission is to get their weights and calculate the average weight. Each person will enter their weight. Since we know how many people will enter their weights, we can hold the values inside the array. However, assigning each value to the specific index by hand is very tedious and boring task. What would we do if we had to calculate the average weight of 1000 people? Luckily, with a little help of a for loop we can easily solve this issue. Examine the below code:

`
#include <stdio.h>
int main() {
  int weights[10];
  int i;
  for( i=0; i<10; i++) {
    scanf("%d",weights[i]);
  }
}
`
    
(If you do not know how `scanf()` method works, go ahead and search for it)

There is nothing much above to talk about. In order to understand what is happening, you need to know `scanf()` and `for loop`, the rest is what we have talked about.

Exercise
--------

* I want you to create copy of `grades` array and put values into another array where the indexes are even. Then print out the new array with one space between them.

Tutorial Code
-------------

    #include <stdio.h>

    int main() {
      float grades[10] = { 100.0, 68.2, 78.8, 22.6, 65,8, 21.2, 98.6, 80.6, 67.0, 90.0 };
      /* TODO: define the new array here */
      

      /* TODO: copy values into the new array

      /* TODO: print out the values in the new array

      return 0;
    }

Expected Output
---------------

    100.0 78.8 65.8 98.6 67.0 

Solution
--------

    #include <stdio.h>

    int main() {
      float grades[10] = { 100.0, 68.2, 78.8, 22.6, 65,8, 21.2, 98.6, 80.6, 67.0, 90.0 };
      /* TODO: define the new array here */
      float newArray[5];

      /* TODO: copy values into the new array
      int i, index = 0;
      for( i=0; i<10; i++ ) {
        if ( i % 2 == 0 ) {
          newArray[index] = grades[i];
          index++;
        }
      }

      /* TODO: print out the values in the new array
      for ( i=0; i<5; i++ ) {
        printf("%d ", newArray[i]);
      }

      return 0;
    }
