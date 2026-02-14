# Assignment2

EDS Lab Assignments: 

1.To accept students five courses marks and compute his/her result. Student is passing scores mnarks equal to and above 40 in each course.
If student scores aggregate greater than 75 percentage, then the grade is distinction.
If aggregate is greater than or equal to 60 and less than 75 then the grade is first division.
If aggregate is greater than or equal 50 and less than 60, then the grade is second division.
If aggregate is greater than or equal 40 and less than 50, then the grade is third division.

python code:

marks = []
for i in range(1, 6):
    m = int(input(f"Enter marks for subject {i}: "))
    marks.append(m)
    
passed = True
for m in marks:
    if m < 40:
        passed = False
        break

if not passed:
    print("Result: FAIL")
else:
    total = sum(marks)
    percentage = total / 5

    print("Result: PASS")
    print("Percentage:", percentage)

    if percentage > 75:
        print("Grade: Distinction")
    elif percentage >= 60:
        print("Grade: First Division")
    elif percentage >= 50:
        print("Grade: Second Division")
    elif percentage >= 40:
        print("Grade: Third Division")

2.Solve the Fibonacci sequence using recursive function in Python.

def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2)

n = int(input("Enter number of terms: "))

print("Fibonacci Sequence:")
for i in range(n):
    print(fibonacci(i), end=" ")

3.Write a Python program to print different patterns.

Pattern 1:right angled triangle

n = 5
for i in range(1, n+1):
    print("*" * i)

Pattern 2:number pattern

n = 5
for i in range(1, n+1):
    for j in range(1, i+1):
        print(j, end="")
    print()
    
