The Non-Attacking Queens Puzzle is a programming problem that involves arranging all queens on a chessboard so that they cannot attack each other. Queens can attack horizontally, vertically, and diagonally. Therefore, we need to arrange the queens so that no queen is in the same row, column, or diagonal as another queen. We can use recursive backtracking in Java to find all possible solutions. In a standard eight by eight chessboard, there are ninety-two possible solutions.

The best way to solve this problem is to break it down into more manageable chunks. I have made a template with three primary helper methods. The first method checks if a given position is valid for a queen. Copy the template and complete `canPlace()`. Manually place a queen in the first row and column. Call `canPlace()` to see if you can place a queen in the first row or column. Also, check if you can place a queen in the same diagonal. If each of the three trials returns false, your code is working correctly.

Next, I recommend completing the `printSolution()` method. Having a completed `printSolution()` method at your disposal will allow you to call it anywhere in your code if you need to debug. Try calling `printSolution()` to see if it prints out a blank board. Then, move on to the solve method. If you are having trouble completing the `solve()` method, call `printSolution()` at the point where you think your code is failing.

The last step is to tie everything together. Remove any test code from `main()`. Initialize the `NonAttackingQueens` class and call `solve()` starting at row zero. Were you able to get ninety-two solutions?

{% highlight java %}
public class NonAttackingQueens {
    // The chessboard
    private int[][] board;
    
    // The size of our chessboard. This sets an 8 x 8 chessboard.
    final int NUM_QUEENS = 8;

    // Constructor, Initialize the board
    public NonAttackingQueens() {
    	board = new int[NUM_QUEENS][NUM_QUEENS];
    }
    
    // Determine if a queen can be placed in the given row and column.
    // Return true for valid placement, otherwise return false
    private boolean canPlace(int row, int col) {
    	// If there is already a queen in this row, return false
        // To accomplish this, loop through all of the columns in the row.
        // If there is a queen in any of the columns, return false
    	
    	// If there is already a queen in this column, return false
        // To accomplish this, loop through all of the rows in this column.
        // If there is a queen in any of the rows, return false

    	// Check up-left diagonal. Make a loop that starts at the row and col parameters.
        // Continue running the loop until the row AND column are greater than or equal to zero.
        // Decrement the row and column for each iteration. If there is a queen in the current row and column, return false.
    	
        // Check up-right diagonal. Make a loop that starts at the row and col parameters.
        // Continue running the loop until the row AND column are greater than or equal to zero.
        // Decrement the row and increment column for each iteration. If there is a queen in the current row and column, return false.
        
        // If we made it to this point, it means that this row and col is a valid placement. Return true.
    }
    
    // Run our recursive solve function.
    public void solve(int row) {
        // If the row is less than NUM_QUEENS, continue checking. Otherwise, print a solution.
        // To continue checking, iterate over all columns in the row. 
        // If you can place in the current column and row, place a queen in that position.
        // Recurse by calling solve with the next row. Then, remove the queen to backtrack.
    }
    
    // Print out a solution
    public void printSolution() {
        // Make two loops that iterate through the rows and columns.
    }
    
    public static void main(String[] args) {
        // initialize the NonAttackingQueens class and solve
    }
}
{% endhighlight %}