Download link :https://programming.engineering/product/hw2-runtime-and-quicksort/


# HW2-Runtime-and-QuickSort
HW2: Runtime and QuickSort
Instructions

Most of this homework does not require coding, but instead, expects you to analyze existing code. Please read each question carefully. We’ve provided an example question and ideal answer in example.txt to help you get started on the runtime analysis questions.

Submitting This Assignment

iCollege

Grading and Corrections

Since this is a written assignment, There are no tests or examples.

This assignment will be graded out of 10 points. The point values of each problem are listed in the title. We will use manual inspection and written rubrics to assign points in a fair, standardized way.

Academic Integrity

Remember that you can consult outside resources and work with other students as long as you write up your own solutions and cite any links or people you received help from within citations.txt.


Q1 Mysterious Function (30 point)

What’s the worst case runtime of the following function? Please remember to define n, provide a tight upper bound.

public static void mystery1(int z) {

System.out.println(z);

if (z >= 10) {

mystery1(z/10);

System.out.println(z);

}

}


Q2 Exponentiation (Fast?) (40 points)

What’s the best case, worst case, and average-case runtime of pow? Assume n = power. Please remember to define n, provide a tight upper bound.

algorithm pow

Input: positive integer b, non-negative integer p

Output: computing b^p (i.e. b raised to power of p)

if p = 0

return 1

else if p = 1

return b

else if p is even

temp = pow(b, p / 2)

return temp * temp

else

return b * b * pow(b, p-2)


Q3 QuickSort (30 point)

Given the QuickSort implementation from class, provide an 18-element list that will take the least number of recursive calls of QuickSort to complete.

As a counter-example, here is a list that will cause QuickSort to make the MOST number of recursive calls:

public static List<Integer> input() {

return Arrays.asList(0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,

0);

}

And here’s the QuickSort algorithm, for convenience:

algorithm QuickSort

Input: lists of integers lst of size N

Output: new list with the elements of lst in sorted order

if N < 2

return lst

pivot = lst[N-1]

left = new empty list

right = new empty list

for index i = 0, 1, 2, … N-2

if lst[i] <= pivot

left.add(lst[i])

else

right.add(lst[i])

return QuickSort(left) + [pivot] + QuickSort(right)
