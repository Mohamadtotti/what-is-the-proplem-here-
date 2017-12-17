# what-is-the-proplem-here-
/**
 * helpers.c
 *
 * Helper functions for Problem Set 3.
 */

#include <cs50.h>

#include "helpers.h"

/**
 * Returns true if value is in array of n values, else false.
 */
bool search(int value, int values[], int n)
{

    if(value == values[n])
    {
        return true;
    }

    else
    {
        // TODO: implement a searching algorithm
        int start = 0, end = n-1;

        while(start <= end)
        {
            int mid = (start + end) /2;

            if(value == values[mid])
            {
                return true;
            }
            else if(value < values[mid])
            {
                end = mid - 1;
            }
            else
            {
                start = mid + 1;
            }
        }
    return false;

    }

}

/**
 * Sorts array of n values.
 */
void sort(int values[], int n)
{


    // TODO: implement a sorting algorithm
    int temp;
    int swap_counter = 0;
    while(swap_counter != 0)
    {
        for(int i = 1; i < n; i++)
        {
            if(values[i - 1] < values[i])
            swap_counter++;
            temp = values[i];
            values[i] = values[i - 1];
            values[i - 1] = temp;
        }

    }
    return;
}
