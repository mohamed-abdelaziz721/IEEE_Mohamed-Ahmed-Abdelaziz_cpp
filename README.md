## Tabel Of Content

- [Pointer Declaratrion And Assigning](#heading)
  * [Sub-heading](#sub-heading)
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
cout << "var:"<< var << endl;  
```
**notice:** 
* we used `*` after the data type to declare a pointer.
* `var`is not a pointer.
* we stored `var` address into `ptr`.
* we used `*` **dereference operator** to print the value stored in this address.
* we can change the `var` content by working with pointers. 

> *note* `*ptr`  has a value and `&var` is an address so we cannot write `*ptr = &var`.
>  `ptr` is an address and `var` has a value so we cannot write `ptr = var`


### Sub-heading

This is an h2 heading

#### Sub-sub-heading

This is an h3 heading

## Heading

This is an h1 heading

### Sub-heading

This is an h2 heading

#### Sub-sub-heading

This is an h3 heading


### Support or Contact

Having trouble with Pages? contact me [Mohamed.ahmed997@eng-st.cu.edu.eg](Mohamed.ahmed997@eng-st.cu.edu.eg) and I’ll help you sort it out.
