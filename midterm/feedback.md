# Notes on the Midterm

* _Correctness    (out of 40):_ 38
* _Good Practices (out of 10):_ 9
* _Docs / Testing (out of 10):_ 1

_Details on the grading criteria for the midterm can be found on [Canvas](https://canvas.slu.edu/courses/28045/rubrics/23671)._

Overall, nicely done.

Just a note on convention - when you open a file and then read all the contents in using `json.load(f)`, you can move the rest of your code outside the `with` block.  At that point, Python is done reading from the file and you can let it close the file.

You only included docstrings and tests in your first function. Those were a required part of the midterm. I've deducted 9 points from the _Docs / Testing_ score.

Each of your functions opens the `/data/negotiated_rates.json` file instead of the `file` parameter that is passed into it.  Your code should be able to work with any file location that is passed into it. I've deducted 1 point total from _Correctness_ for this.


## Step 1
* Note that docstrings have to go after the `def` line for your function. Otherwise Python doesn't recognize them as docstrings.

## Step 2
* No additional comments.

## Step 3
* Your code should have reused the `get_rate()` function that you already wrote rather than repeating all of that code over again. I deducted 1 point from _Good Practices_ for this.
* Because you didn't reuse the `get_rate()` function and didn't test for non-matching condition, you ran into an indenting issue that lead to problems when a match wasn't found. Your code runs the `if weekday` and `if pat_age` conditions for every allowed amount, not just those where the billing code and service code match. They aren't indended under the `if bill_code ...` condition. I've deducted 1 point from _Correctness_ for this.

## Step 4
* Your code, as submitted, didn't work.  It had a few minor syntax issues.
* Once I made it run, it surfaced the second issue on step 3 above.