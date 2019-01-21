# Sudoku-Generator
Sudoku generator using C++
Sudoku Generator--(RC2427)

In Sudoku we have 9x9 array that we have to fill with numbers ranging from 1 to 9 following certain rules
1)The number should not repeat int the same row.
2)The number should not repeat in the same column.
3)The number should not repeat int the 3x3 box.

-->First we create a class sudoku which would contain data members=> two 9x9 arrays->one->without zeros(data[i][j]) and the other with zero's(arr[i][j]) and methods/member functions to check
   if number is repeated in row column or 3x3 block also one for checking if the number/element is zero or not.
-->Fill the data[i][j] wiht zeros.    
-->Now first to generate Numbers randomly I have used "default_random_engine"(generates psuedo random numbers)/(or you can yous rand() and srand()), uniform_int_distribution
   for more info on these->http://www.cplusplus.com/reference/random/default_random_engine
   (note :- rand() and srand() can also be used here instead of the above two)
-->In psuedogen() method the 9x9 array block is been filled with random numbers only in few spaces(which are also randomly generated i.e. 'i' and 'j' are randomly generated too).
   By doing this we can get a new sudoku puzzle each time we run the program or else we will be stuck with one single sudoku puzzle with first row or column as 1 to 9 numbers serially.
  
-->Now in sudogen() method we actually generate the complelte puzzle.Now in this method first we check for elemnt position with the number zero in it.
   Then inside a for loop(for(num=1 to 9)) we check if num can be inserted int found positon or not by using the check function if true then the number is inserted
   here is the part where bactracking algotrithm is used we call the function sudogen() again and check if return true or not if not true the we assgin the postion as zero again,
   then the loop is incremented and again checked.To uderstand this more clearly checkout the N-queens bactracking algorithm.
-->Copy elemnts of data[i][j] to arr[i][j]
-->For filling zeros randomly generate 'i' and 'j' randomly for arr then insert the zeros there.
    
