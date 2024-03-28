#!/bin/bash

# Prompt user to enter a number
echo "Enter a number:"
read number

# Check if the input is valid
if ! [[ "$number" =~ ^[0-9]+$ ]]; then
    echo "Error: Please enter a valid number."
    exit 1
fi

# Prompt user for input
echo "Do you want to see a full multiplication table from 1 to 10 or a partial table within a specified range?"
echo "Enter 'f' for a full table or 'p' for a partial table:"
read choice

# Check user's choice and display corresponding multiplication table
case "$choice" in
    f)
        echo "Multiplication table for $number (from 1 to 10):"
        for (( i=1; i<=10; i++ )); do
            result=$((number * i))
            echo "$number x $i = $result"
        done
        ;;
    p)
        echo "Enter the starting range (e.g., 2):"
        read start
        echo "Enter the ending range (e.g., 5):"
        read end

        # Check if the range inputs are valid numbers
        if ! [[ "$start" =~ ^[0-9]+$ ]] || ! [[ "$end" =~ ^[0-9]+$ ]]; then
            echo "Error: Please enter valid numbers for the range."
            exit 1
        fi

        echo "Partial multiplication table for $number (from $start to $end):"
        for (( i=start; i<=end; i++ )); do
            result=$((number * i))
            echo "$number x $i = $result"
        done
        ;;
    *)
        echo "Invalid choice. Please enter 'f' or 'p'."
        exit 1
        ;;
esac
