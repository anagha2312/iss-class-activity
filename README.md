#iss class activity 2
   in  Line 1:
        def is_narc(n) is wrong because A colon (:) was missing.
         Corrected: def is_narc(n):
   in  Line 3-4:
        num_str == str(n) is wrong so we Used == instead of =, which is incorrect.
         Corrected: num_str = str(n)
        num_digits == len(num_str) → Same mistake as above.
         Corrected: num_digits = len(num_str)
   in  Line 6:
        sum(int(digit) *** num_digits for digit in num_str) is wrong because  *** is invalid in Python.
         Corrected: sum(int(digit) ** num_digits for digit in num_str)
   in  Line 10:
        def print_narcis_numbers(start end) was wrong because there was A missing comma (,) between parameters.
         Corrected: def print_narcis_numbers(start, end):
    in Line 12:
        for num in range(start, end + 1) is wrong  A colon (:) was missing at the end.
         Corrected: for num in range(start, end + 1):
    in Line 13:
        if is_narcissistic(num) is wrong  The function name should be is_narc(num).
         Corrected: if is_narc(num):
    in Line 16:
        print_narc_numbers(1000, 5000) is an  Incorrect function name.
         Corrected: print_narcis_numbers(1000, 5000)

Final Corrected Code:

def is_narc(n):
    """Check if a number is narcissistic."""
    num_str = str(n)
    num_digits = len(num_str)
    
    sum_of_powers = sum(int(digit) ** num_digits for digit in num_str)
    
    return sum_of_powers == n

def print_narcis_numbers(start, end):
    """Print all narcissistic numbers in a given range."""
    for num in range(start, end + 1):
        if is_narc(num):
            print(num)

print_narcis_numbers(1000, 5000)

Output on Running the Code
1634
