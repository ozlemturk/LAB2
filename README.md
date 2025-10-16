# LAB2


Sorular
1-why can’t we rely on CPU execution time to measure algorithm efficiency?

Because cpu execution depends on hardware and software like operation system, programming language, ram.… and these factors can be change in different computers.
But algorithm efficiency, we look at input size.
Therefore, we use asymptotic analysis (big O notation) instead of CPU to execution time 

2-How many operations does this code execute?
	int sum = 0;
	sum = sum + 5;
	
	first row -> 1 operation
	second row -> sum + 5 ( 2 operation) and sum = (1 operation ) => so this is 3 operation 
	but in (big O notation) this is 1 operation because big o notation has logn, n ,n!, x^2…. 
	therefore we should say this is 1 operation.

3-Give the final time complexity of the code
	a) int sum = 0;
	     for(int i = 0; i < n; i++) {
	         sum += i;
	     }


    	first row -> 1 operation
    	second row -> int i = 0 (1 operation)
    				 i < n  (n + 1operation)
    				 i++   (n operation)
    	third row ->  sum += i => sum = sum + i, so n + n operation 2n
    
    	so we have 4n + 3 operation but in big O we say that n operation O(n)


	b)
		int sum = 0;
		for(int i ‎ = 0; i <n ; i++) {
			for(int j = 0; j <n ; j++) {
				sum += i + j;			
			}
		}

		first row -> 1 operation
    each for loop n operation but 2 for loop n^2 because its nested
		2 for loop -> n^2 operation
		fourth row -> n^2 operation

		so we have 2(n^2) + 1 operation and in big o we say that n^2  O(n^2)


	c)

		int n = 1024;
		int count = 0;
		while(n > 1) {
			n = n/ 2;
			count ++;
			System.out.println(“n = ” + n);
		}
		System.out.println(“Total divisions: ” + count);


		first row -> 1 operation
		second row -> 1 operation
		while loop -> log(n)
		last row -> 1 operation
		
		log(n) + 3 operation and in big O we say that log(n) operation that is equal to O(log(n))
		


