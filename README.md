### NAME : V.B.LAKSHA

### REG NO.: 212224220051
# Experiment-2
Write a program in Python language for Matrix multiplication fails. Introspect the causes for its failure and write down the possible reasons for its failure. 
## Aim
Write a python program for matrix multiplication and inspect for failures. 

## Algorithm
1.	Start the program.
2. Create empty list formatrix1, matrix2 and result.
3. Get the rows and columns count from the user.
4. Get the values of two matrix.
5. Perform matrix multiplication and store the answer in result.
6. Stop the program. 

## Program
```
try:
    r1 = int(input("Enter number of rows for Matrix A: "))
    c1 = int(input("Enter number of columns for Matrix A: "))
    print(f"Enter elements row by row ({r1}x{c1}):")
    A = [list(map(int, input().split())) for _ in range(r1)]

    r2 = int(input("\nEnter number of rows for Matrix B: "))
    c2 = int(input("Enter number of columns for Matrix B: "))
    print(f"Enter elements row by row ({r2}x{c2}):")
    B = [list(map(int, input().split())) for _ in range(r2)]

    if c1 != r2:
        print("\nMatrix multiplication not possible!")
        print(f"Columns of A ({c1}) != Rows of B ({r2})")
    else:
        result = [[0 for _ in range(c2)] for _ in range(r1)]
        for i in range(r1):
            for j in range(c2):
                for k in range(c1):
                    result[i][j] += A[i][k] * B[k][j]

        print("\nResultant Matrix:")
        for row in result:
            print(row)

except ValueError as ve:
    print("Input Error:", ve)
except Exception as e:
    print("Unexpected Error:", e)
```
## Output

<img width="1855" height="355" alt="Screenshot 2025-08-30 101640" src="https://github.com/user-attachments/assets/a5f8a5c3-e400-430d-8198-6b9768a6012a" />

## Result
Thus the python program for Matrix multiplication is executed.
