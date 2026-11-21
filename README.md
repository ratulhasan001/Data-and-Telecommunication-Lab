# Data and Telecommunication Lab

MATLAB scripts from the Data and Telecommunication sessional (lab) course of the B.Sc. in Computer Science and Engineering at BAUET. The first two labs introduce MATLAB itself (loops, conditionals, matrices and plotting). Labs 3 and 4 implement and plot digital line-coding schemes: unipolar NRZ and RZ, polar NRZ-L and NRZ-I, and bipolar AMI and pseudoternary encoding.

## Contents

### [lab-01](lab-01) – MATLAB basics

| File | What it does |
|---|---|
| [primes_and_matrix_operations.m](lab-01/primes_and_matrix_operations.m) | Prints the primes in a user-given range by trial division up to √i, then adds and multiplies two 3 × 3 matrices. *Line 3 has a stray character (`input("")s`), so the script stops with a syntax error until it is removed.* |

### [lab-02](lab-02) – Loops, conditionals and plotting

| File | What it does |
|---|---|
| [sum_of_series.m](lab-02/sum_of_series.m) | Sum 1 + 2 + … + n using the closed form n(n + 1)/2. |
| [factorial.m](lab-02/factorial.m) | n! with a `for` loop. |
| [fibonacci.m](lab-02/fibonacci.m) | First n Fibonacci numbers (starting 0, 1) stored in a vector. |
| [armstrong_number.m](lab-02/armstrong_number.m) | Armstrong-number check: sum of each digit raised to the number of digits. |
| [perfect_number.m](lab-02/perfect_number.m) | Perfect-number check: sums the proper divisors found in O(√n). |
| [count_digit_one_parity.m](lab-02/count_digit_one_parity.m) | Counts the digit `1` in a number and reports whether that count is odd or even. |
| [plot_function.m](lab-02/plot_function.m) | 2-D plotting examples: y = x, y = x², sin x and cos x with labels, a legend and a grid, and polynomial and exponential curves. *Every line is commented out; uncomment a block to run it.* |

### [lab-03](lab-03) – Unipolar line coding

| File | What it does |
|---|---|
| [line_coding_notes.txt](lab-03/line_coding_notes.txt) | Plain-text notes on signal elements, data rate, and the families of line codes (unipolar, polar, bipolar, multilevel, multitransition). *This is not executable MATLAB.* |
| [unipolar_nrz.m](lab-03/unipolar_nrz.m) | Unipolar NRZ: bit 1 is +V and bit 0 is 0 V for the whole bit period. Plots the waveform for the stream `1 0 1 1 0 1 0 0 1`, sampled at 100 Hz. |
| [unipolar_rz.m](lab-03/unipolar_rz.m) | Unipolar RZ: bit 1 is +V for the first half of the bit and returns to 0 V for the second half. Uses the same bit stream. |

### [lab-04](lab-04) – Polar and bipolar line coding

| File | What it does |
|---|---|
| [polar_nrz_l.m](lab-04/polar_nrz_l.m) | Polar NRZ-L: the level encodes the bit (0 → +1, 1 → −1). The bit values are drawn above the waveform. |
| [polar_nrz_i.m](lab-04/polar_nrz_i.m) | Polar NRZ-I: a 1 inverts the current level and a 0 keeps it. |
| [bipolar_ami.m](lab-04/bipolar_ami.m) | Bipolar AMI: 0 → 0 V; each 1 alternates between +1 and −1. |
| [bipolar_pseudoternary.m](lab-04/bipolar_pseudoternary.m) | Pseudoternary, the opposite of AMI: 1 → 0 V; each 0 alternates between +1 and −1. |

## Running the scripts

Run the scripts in MATLAB, or in GNU Octave, which runs these scripts as well. Start from the repository root:

```matlab
cd lab-04
bipolar_ami          % opens a figure with the AMI waveform
```

From a shell with Octave installed:

```bash
octave --persist lab-04/bipolar_ami.m
```

The Lab 1 and Lab 2 scripts read their input with `input("")`, so type a number at the prompt. The bit streams in Labs 3 and 4 are hard-coded at the top of each script (`bitStream = [...]` or `m = [...]`); edit them to encode other data.

## Author

Ratul Hasan · [ratulhasan.dev](https://ratulhasan.dev)
