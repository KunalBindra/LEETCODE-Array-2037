# LEETCODE-Array-2037
Certainly! Let's walk through a dry run of the `minMovesToSeat` method in the `Solution` class with an example to understand how it works.

Here is the method again for reference:

```java
class Solution {
  public int minMovesToSeat(int[] seats, int[] students) {
    int res = 0;

    Arrays.sort(seats);
    Arrays.sort(students);

    for (int i = 0; i < seats.length; ++i)
      res += Math.abs(seats[i] - students[i]);

    return res;
  }
}
```

### Example:
Let's use the following example arrays:
- `seats = [3, 1, 5]`
- `students = [2, 7, 4]`

### Step-by-Step Dry Run:

1. **Initial arrays:**
   - `seats = [3, 1, 5]`
   - `students = [2, 7, 4]`

2. **Sorting the arrays:**
   - `Arrays.sort(seats)` results in `seats = [1, 3, 5]`
   - `Arrays.sort(students)` results in `students = [2, 4, 7]`

3. **Initialize the result variable:**
   - `res = 0`

4. **Iterate through the arrays and compute the total moves:**

   - **First iteration (i = 0):**
     - Calculate the absolute difference: `Math.abs(seats[0] - students[0]) = Math.abs(1 - 2) = 1`
     - Add the difference to `res`: `res = res + 1 = 0 + 1 = 1`

   - **Second iteration (i = 1):**
     - Calculate the absolute difference: `Math.abs(seats[1] - students[1]) = Math.abs(3 - 4) = 1`
     - Add the difference to `res`: `res = res + 1 = 1 + 1 = 2`

   - **Third iteration (i = 2):**
     - Calculate the absolute difference: `Math.abs(seats[2] - students[2]) = Math.abs(5 - 7) = 2`
     - Add the difference to `res`: `res = res + 2 = 2 + 2 = 4`

5. **Return the result:**
   - The final value of `res` is `4`.

### Conclusion:
The method calculates the minimum number of moves required to seat all students by sorting both the `seats` and `students` arrays, then summing the absolute differences between corresponding elements. In this example, the minimum number of moves needed is `4`.
