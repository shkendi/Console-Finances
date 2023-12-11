# Unit 4 Challenge: Console Finances

Depoyed link: https://shkendi.github.io/Console-Finances/

## Overview

In this challenge, I'll be using the concepts I've learned to complete the required activity. This activity presents a real-world situation in which my newfound JavaScript skills will come in handy. My task is creating code for analyzing the financial records of a company. I have been provided with a financial dataset in the `starter/index.js` file and have to follow the instructions as below.

## Instructions

1. Create a new GitHub repo called `Console-Finances`. Then, clone it to your computer.

2. Copy the starter files in your local git repository.

You have been given a dataset composed of arrays with two fields, Date and Profit/Losses.

## Brief

Write JavaScript code that analyzes the records to calculate each of the following:

- The total number of months included in the dataset.

- The net total amount of Profit/Losses over the entire period.

- The average of the **changes** in Profit/Losses over the entire period.

  - You will need to track what the total change in Profit/Losses are from month to month and then find the average.
  - (`Total/(Number of months - 1)`)

- The greatest increase in Profit/Losses (date and amount) over the entire period.

- The greatest decrease in Profit/Losses (date and amount) over the entire period.

When you open your code in the browser your resulting analysis should look similar to the following:

```text
Financial Analysis
----------------
Total Months: 86
Total: $38382578
Average Change: -2315.12
Greatest Increase in Profits/Losses: Feb-2012 ($1926159)
Greatest Decrease in Profits/Losses: Sep-2013 ($-2196167)
```

## Getting into coding

1. Following the instructions, I started by creating a new repository which I named it 'Console-Finances'. I copied the starter code with index.html and index.js files in it.

2. I then started getting the data of the given array such as the number of months. I console loged everything step by step to check if I got the right result. ![Alt text](<Screenshot 2023-12-10 at 21.26.51.png>)

const totalMonths = finances.length

3. Next, I found the total amount of profits/loses over the entire period using the .reduce method to calculate the sum of all numbers in the array.
   The reduce() method starts from the first element of the array (or the initial value if provided) and iterates through each element of the array. The accumulator starts at 0 (zero). Console log the result to check if there are any errors showing.

![Alt text](<Screenshot 2023-12-11 at 12.37.24.png>)

const total = finances.reduce((acc, [, value]) => acc + value, 0)

4. Following, I had to calculate the average change in Profits/Loses over the entire period. I started by calculating the total of all changes starting from index 0 and then to find the average ghange I divided the whole sum of changes with the length of the finances array from index 0 (finances.length - 1). I used .toFixed(2) method to round up to the nearest houndridth and returning it as a string. Console loged to check the result.

5. The next task was to find out the greatest increase in Profits/Loses over the entire period. I used Math.max() method to check and find the maximum value of the entire finances array which I assigned it to 'maxIncrease' and then assigned the greatestIncrease === maxIncrease. Console loged to check the result are correct.

![Alt text](<Screenshot 2023-12-11 at 20.56.37.png>)

6. The last task of the challenge was to find out the greatest decrease in Profits/Loses over the entire period. For this task I used the Math.min() method to loop over the array and find out the minimum value which I assigned it as 'minDecrease' of the entire array of finances and then I assigned greatestDecrease === minDecrease and console loged the result.

![Alt text](<Screenshot 2023-12-11 at 20.59.15.png>)

7. I console loged everithing to make sure that all code is working correctly and the result was as below.

![Alt text](<Screenshot 2023-12-11 at 21.10.50.png>)

![Alt text](<Screenshot 2023-12-11 at 21.09.22.png>)
