# Numerical Data Types in Python

- **Integers:** Represent whole numbers without any decimal points. Examples include 5, 0, large whole numbers, and negative whole numbers like `-10`.    
- **Floating-point numbers:** Represent numbers with decimal points, used for non-integers. Examples include `2.5` and pi (3.14159).

Python supports standard arithmetic operations: `addition (+), subtraction (-), multiplication (*), and division (/)`.

>[!IMPORTANT]
>If an integer and a floating-point number are mixed in an operation the result will always be a floating-point number.

For addition, subtraction, and multiplication of two integers, the result will always be an integer. For division (/) of two integers, the result will always be a floating-point number, even if the mathematical answer is a whole number . This is because not all integer divisions yield an integer result, whereas other operations between integers always do.
## Additional Operators

Python also provides specialized operators for numerical calculations:

- **Integer Division Operator (`//`):** This operator returns how many times one whole number divides into another, discarding any remainder. 
- **Modulo Operator (`%`):** This operator returns the remainder from an integer division operation.
- **Exponential Operator (`**`)**: This operator performs exponential calculations, raising one number to the power of another.