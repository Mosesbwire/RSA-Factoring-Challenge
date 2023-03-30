#!/usr/bin/python3
""" Module factors:
    This module factorizes numbers into their constituents
    As well as try to get the prime numbers used in RSA encryption key
"""

import sys


def factorize_numbers(input_file):
    """Reads numbers from file line by line
    Factorizes each number in the file
    Prints the results to stdout
    Args:
        input_file (file): File to read numbers from
    """
    with open(input_file, 'r') as file:
        for num in file:
            factors = factorize_int(num)
            num = num.strip()
            print("{}={:d}*{:d}".format(num, factors[0], factors[1]))


def factorize_int(num):
    """ Factorizes a number
    Args:
        num (int): Parameter to factorize
    Returns:
        list: Length 2, with the two numbers that make the parameter num
    """
    factorized = False
    factors = []
    x = 2

    while not factorized:
        if int(num) % x == 0:
            factors.append(int(num) // x)
            factors.append(x)
            factorized = True
        x += 1

    return factors


if __name__ == "__main__":
    if len(sys.argv) == 2:
        factorize_numbers(sys.argv[1])
