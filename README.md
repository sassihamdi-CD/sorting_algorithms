# Sorting Algorithms & Big O Notation

![C](https://img.shields.io/badge/Language-C-blue.svg)
![GitHub last commit](https://img.shields.io/github/last-commit/username/sorting_algorithms)
![License](https://img.shields.io/github/license/username/sorting_algorithms)

## Table of Contents
- [Background Context](#background-context)
- [Learning Objectives](#learning-objectives)
- [Copyright - Plagiarism](#copyright---plagiarism)
- [Requirements](#requirements)
- [Data Structure and Functions](#data-structure-and-functions)
- [Sorting Algorithms & Big O Notation](#sorting-algorithms--big-o-notation)
    - [1. Bubble sort](#1-bubble-sort)
    - [2. Insertion sort](#2-insertion-sort)
    - [3. Selection sort](#3-selection-sort)
    - [4. Quick sort](#4-quick-sort)
- [Tests](#tests)
- [Quiz questions](#quiz-questions)

## Background Context
This project is aimed to be completed by teams of two students. Each team should pair program for at least the mandatory part.

## Learning Objectives
Upon completion of this project, you are expected to be able to explain the following topics to anyone, without the help of Google:

1. At least four different sorting algorithms
2. What is the Big O notation, and how to evaluate the time complexity of an algorithm
3. How to select the best sorting algorithm for a given input
4. What is a stable sorting algorithm

## Copyright - Plagiarism
You are tasked to come up with solutions for the tasks below yourself to meet the learning objectives stated above. You will not meet the objectives by copying and pasting someone else’s work. Publishing any content of this project is strictly forbidden and will result in removal from the program.

## Requirements
General:
- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project, is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- Unless specified otherwise, you are not allowed to use the standard library. Any use of functions like printf, puts, … is totally forbidden.
- The prototypes of all your functions should be included in your header file called sort.h
- Don’t forget to push your header file
- All your header files should be include guarded
- A list/array does not need to be sorted if its size is less than 2.

## Data Structure and Functions
For this project, you are given the following print_array and print_list functions:

```c
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}

#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}




Our files print_array.c and print_list.c (containing the print_array and print_list functions) will be compiled with your functions during the correction. Please declare the prototype of the functions print_array and print_list in your sort.h header file.

Please use the following data structure for the doubly linked list:

/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;

### Sorting Algorithms & Big O Notation
+ Bubble sort
/**
 * bubble_sort - Sorts an array of integers in ascending order using the Bubble sort algorithm
 *
 * @array: The array to be sorted
 * @size: Number of elements in @array
 */
void bubble_sort(int *array, size_t size);

### Big O Notation:
+ Best case: O(n)
+ Average case: O(n^2)
+ Worst case: O(n^2)

### Insertion sort
'''
/**
 * insertion_sort_list - Sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm
 *
 * @list: The list to be sorted
 */
void insertion_sort_list(listint_t **list);
'''

### Big O Notation:
Best case: O(n)
Average case: O(n^2)
Worst case: O(n^2)

'''
/**
 * selection_sort - Sorts an array of integers in ascending order using the Selection sort algorithm
 *
 * @array: The array to be sorted
 * @size: Number of elements in @array
 */
void selection_sort(int *array, size_t size);
'''

### Quick sort
'''
/**
 * quick_sort - Sorts an array of integers in ascending order using the Quick sort algorithm
 *
 * @array: The array to be sorted
 * @size: Number of elements in @array
 */
void quick_sort(int *array, size_t size);
'''
### Big O Notation:
Best case: O(nlog(n))
Average case: O(nlog(n))
Worst case: O(n^2)

## Tests

You can use the provided main.c files for testing the sorting algorithms. For larger sets of random integers, you may use Random.org for generating test data.



