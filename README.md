# call-by-value-call-by-reference


AIM:

          To study and implement Pointer Operations (Call by value and Call by reference).


SOFTWARE USED:

          VS Code 


OBJECTIVE:


    - To understand and implement the concept of pointer operations in C.
    - To differentiate between:
        1. Call by Value: Passing arguments by copying actual values.
        2. Call by Reference: Passing arguments using pointers to modify original values.
    - To observe how memory addresses and variable values interact during function calls.


 THEORY:

 In C programming, understanding how data is passed between functions is essential
 for writing efficient and predictable code. Two fundamental techniques for passing
 arguments are:

    1. Call by Value
    2. Call by Reference

 -------------------------------------------------------------------------------
 1. CALL BY VALUE:
 -------------------------------------------------------------------------------
 - The actual value of the variable is passed to the function.
 - The function works on a copy of the variable.
 - Changes made inside the function do NOT affect the original variable.
 - Separate memory is allocated for the copy inside the function.

 Example:
    void modify(int x) {
        x = x + 10;
    }

    int main() {
        int a = 5;
        modify(a);
        printf("%d", a); // Output: 5
    }

 -------------------------------------------------------------------------------
 2. CALL BY REFERENCE:
 -------------------------------------------------------------------------------
 - The address of the variable is passed to the function using pointers.
 - The function works on the original variable via its memory address.
 - Changes made inside the function DO affect the original variable.
 - No new memory is allocated; the function accesses the same memory location.

 Example:
    void modify(int *x) {
        *x = *x + 10;
    }

    int main() {
        int a = 5;
        modify(&a);
        printf("%d", a); // Output: 15
    }

 -------------------------------------------------------------------------------
 FLOW OF EXECUTION:
 -------------------------------------------------------------------------------

 CALL BY VALUE:
    main()
      |
      |---> Pass value to function
                  |
                  |---> Function creates a copy
                  |---> Modifies copy
                  |---> Returns (original unchanged)

 CALL BY REFERENCE:
    main()
      |
      |---> Pass address to function
                  |
                  |---> Function accesses original variable via pointer
                  |---> Modifies original directly
                  |---> Returns (original changed)

 -------------------------------------------------------------------------------
 MEMORY VISUALIZATION:
 -------------------------------------------------------------------------------

 CALL BY VALUE:
    Main Memory:
        a = 5

    Function Memory:
        x = 5 (copy)

 CALL BY REFERENCE:
    Main Memory:
        a = 5

    Function Memory:
        x = &a (pointer to original)
        *x = 15 (modifies original)

 -------------------------------------------------------------------------------
 APPLICATIONS:
 -------------------------------------------------------------------------------
 - Use Call by Value when:
     • You want to protect original data.
     • Working with small, simple data types.

 - Use Call by Reference when:
     • You need to modify original data.
     • Working with large structures (arrays, structs).
     • Optimizing performance by avoiding data duplication.

         
SAMPLE OUTPUT:

          Pass by value code-
                        a is:5
                        b is:2
                        
          Pass by pointer:
                        Original value of a is:5
                        original value of b is:2
                        Swapped value of a is:2
                        Swapped value of b is:5 

          Call by reference:
                        Original value of a is:12
                        original value of b is:21
                        Swapped value of a is:21
                        Swapped value of b is:12

         Array modification:
                        Enter a number: 4
                        Before update: 10 20 30 40 50 
                        After update: 4 5 6 7 8 

        Salary increment using pointer:
                        Enter the number of recent projects: 7
                        How many research publications have you done? 5
                        How much profit have you made in last one year? 20k
                        Enter the number of new projects in pipeline: 
                        Sorry! You did not meet the selection criteria.


 CONCLUSION:
 -------------------------------------------------------------------------------
        This experiment helps in understanding how functions interact with variables
 through memory. Mastering pointer operations and the distinction between
 Call by Value and Call by Reference is essential for efficient programming,
 especially in systems programming, embedded systems, and performance-critical
 applications.


          
          
