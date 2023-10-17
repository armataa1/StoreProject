# StoreProject
You must fully implement QueueInterface, ArrayQueue, and LinkedQueue in the code. In JAVA
The checkout area of a local store has eight checkout registers, each with its own line. Due to space constraints, each line can accommodate at most four people. As a result, when all the checkout lines are full, new customers leave the store without making a purchase. 
Simulate this checkout area. Assume an average service time of two minutes per customer. If a new customer arrives every t  minutes, for what value of t will this store serve the most customers and lose the fewest during a 16-hour workday?
The class Store holds an array of registers: private Register [] registers. 
Also, two integer fields: lost and served.
It is a good practice to define named constants: NUM_REGS= 8 and ARRIVAL_TIME set to what you want: it stands for the value t in the problem description. You can also define a constant SERVICE_TIME = 2.0
Don’t forget to create a constructor.
The class Register holds a queue of customers and the current queue length. You need it because the QueueInterface does not provide the method size().
The methods getLineLength, isFull, isEmpty are obvious.
The class Customer holds just one double field: remainingTime.
The main method allocates a store and in a loop calls store.update();
Then output the number of served and the number of lost customers.
What does the method update() mean?
It first updates remaining times for every customer: decrease them by  Store.ARRIVAL_TIME
If the remaining time <= 0, dequeue this customer and increment number of served.
Then it  finds the counter with the shortest line length and  tries to add a customer. If it is not possible (because the line is full), the number of lost is incremented.  If it is possible, enqueue a new customer with appropriate remaining time: SERVICE_TIME if the line is empty or remaining time of the last customer plus SERVICE_TIME. You may need to have the field lastCustomer in the class Register.
These are the suggestions. See the output and decide if it is trustworthy. If not, think about what is wrong.
You may use your own algorithm as long as the ADT Queue is used, and the result is verifiable.
