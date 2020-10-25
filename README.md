## Tabel Of Content

- [Pointer Declaratrion And Assigning ](#heading)
  * [Pointers And Arrays](#sub-heading)
    + [Sub-sub-heading](#sub-sub-heading)
- [Heading](#heading-1)
  * [Sub-heading](#sub-heading-1)
    + [Sub-sub-heading](#sub-sub-heading-1)



# Pointers

> Pointers are variables that store the memory addresses of other variables. For any `variable` we can have its address by `&variable`.


```c++
#include <iostream>
using namespace std;

int main()
{
    // declare variable
    int var1 = 3;
    int var2 = 5;


    // print address of var1
    cout << "Address of var1: "<< &var1 << endl;
    / print address of var2
    cout << "Address of var2: "<< &var2 << endl;

}
```
You will see an output that begin with `0x` which indicate the address of the variable in the memory. 
**notice:** `int` variable has a size of 4 byte in a 64-bit operating system.  


## Pointer Declaratrion And Assigning
```c++
// pointer declaration
int* ptr;
// or int *ptr
  
// assigning address to pointer
int* ptr, var;
var = 10;
ptr = &var;

//accessing the value of the ptr
cout<< "(*ptr):" <<*ptr << endl;   // output: 10

//changing value pointed by the pointer
*ptr = 5;
cout << "var:"<< var << endl;      // output: 5
```
**notice:** 
* we used `*` after the data type to declare a pointer.
* `var`is not a pointer.
* we stored `var` address into `ptr`.
* we used `*` **dereference operator** to print the value stored in this address.
* we can change the `var` content by working with pointers. 

> *note* `*ptr`  has a value and `&var` is an address so we cannot write `*ptr = &var`.

>  `ptr` is an address and `var` has a value so we cannot write `ptr = var`


## Pointers And Arrays
Pointers can store address of cells of an array. 
```c++
int *ptr;
int arr[4] = {1, 2, 3, 4};
 // address of the first element of the array is stored in the pointer ptr
ptr = arr;  // or ptr = &arr[0];
```
Here the pointer points to the address of the first element of the array.


**Navigation through the array using pointers**
```c++
int *ptr;
int arr[4] = {1, 2, 3, 4};
ptr = arr;
// printing address of array elements using pointers
 for (int i = 0; i < 4; ++i)
 {
    cout<< "ptr + " << i << "=" << ptr + i << endl;
    //printing address of array elements 
    // cout<< "&arr[" << i << "] = " << &arr[i] << endl;
 }
 
 
 // printing values of array elements using pointers
 for (int i = 0; i < 4; ++i)
 {
    cout<< "*(ptr + " << i << " ) =" << *(ptr + i) << endl;
    //printing values of array elements 
    // cout<< "arr[" << i << "] = " << arr[i] << endl;
}
```

> If we initialize `ptr  = &arr[1]` we will have 
> ptr - 1  is same as &arr[0]
> ptr + 1  is same as &arr[2]
> ptr + 2  is same as &arr[3]


#### Array name used as a pointer
```c++
#include <iostream>
using namespace std;

int main() {
    int arr[5];
    
   // Insert data using pointer notation
    cout << "Enter 5 numbers: ";
    for (int i = 0; i < 5; ++i) 
    {
        // store input number in arr[i]
        cin >> *(arr + i) ;
    }

    // printing data using pointer notation
    cout << "Array elements: " << endl;
    for (int i = 0; i < 5; ++i) 
    {
        // print value of arr[i]
        cout << *(arr + i) << endl ;
    }
    return 0;
}
```
**notice** we did not declare a pointer, but instead we used the array ame for the pointer notation.
This is an h3 heading

## Heading

This is an h1 heading

### Sub-heading

This is an h2 heading

#### Sub-sub-heading

This is an h3 heading


### Support or Contact

Having trouble with Pages? contact me [Mohamed.ahmed997@eng-st.cu.edu.eg](Mohamed.ahmed997@eng-st.cu.edu.eg) and I’ll help you sort it out.
