#!/usr/bin/python3

import sys


def factorize(n):
    """Return a list of all factor pairs of n."""
    factors = []
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            factors.append((i, n//i))
    return factors


if __name__ == '__main__':
    # Get input file path from command line argument
    try:
        filepath = sys.argv[1]
    except IndexError:
        print('Usage: factors <file>')
        sys.exit(1)

    # Read numbers from input file and factorize them
    with open(filepath, 'r') as f:
        for line in f:
            n = int(line.strip())
            factor_pairs = factorize(n)
            for p, q in factor_pairs:
                print(f'{n}={p}*{q}')
