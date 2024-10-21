# Experiment 9 To study and implement C++ Pointer basics
## Aim:-
To learn about pointers, how to implemnent pointers for different data types, how to make and print an array using pointers.






Pointers are symbolic representations of memory addresses, allowing programs to simulate call-by-reference and handle dynamic data structures. One of the primary uses of pointers is to iterate through elements in arrays or other structures. A pointer holds the address of the variable it points to, which must be of the same data type (such as an integer or string).

### Advantages of Pointers:
- Facilitate dynamic memory allocation
- Allow functions to return multiple values
- Enable modification of the original data
- Provide efficient data transfer between functions
- Optimize memory usage
- Support efficient data structure manipulation
- Enable call-by-reference

### Disadvantages of Pointers:
- Can be challenging to grasp initially
- May lead to errors such as segmentation faults or unintended memory access
- An incorrect pointer value can corrupt memory
- Can cause memory leaks if not handled properly

### Applications of Pointers:
- Allocating new objects on the heap
- Passing functions as arguments to other functions
- Iterating over elements in arrays or data structures

- ## Code:-
```
// utkarsh chaudhary
// 23070123146

#include <iostream>
using namespace std;

int main()
{
    int a = 10;
    int *aptr = &a;
    cout<<"dereferencing the pointer of a: "<<*aptr<<endl;
    *aptr = 20;
    cout<<"updating value using pointer: "<<a<<endl;

    float f = 100.009;
    float *fptr = &f;
    cout<<"value off f"<<f<<endl;
    cout<<"pointer of f"<<fptr<<endl;
    cout<<"dereferencing f "<<*fptr<<endl;
    cout<<"referencing f"<<&f<<endl;

    char ch = 'c';
    char *chptr = &ch;
    cout<<"character: "<<ch<<endl;
    cout<<"pointer of character"<<chptr<<endl;
    cout<<"referncing character: "<<&ch<<endl;
    cout<<"dereferencing"<<*chptr<<endl;

    int arr[] = {5,90,30};
    int *arr_ptr = &arr[3];
    cout<<arr_ptr<<endl;
    cout<<"printing an array by dereferencing its pointers: "<<endl;
    for(int i = 0;i<3;i++)
    {
        cout<<(*(arr+i))<<endl; // printing the array using pointers 
    }

    cout<< "Creating an arrray using pointers: "<<endl;
    int *p = new int[5];
    for(int i = 0;i<5;i++)
    {
        p[i] = 10*(i+1);
    }
    // printing the values 
    cout<< *p<<endl;
    cout<< *p+1<<endl;
    cout<< *(p+1)<<endl;
    cout<<2[p]<<endl;
    cout<<p[2]<<endl;
    *p++;
    cout<<*p;

    return 0;
}
```
