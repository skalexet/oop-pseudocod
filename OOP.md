	Imagine we have an order to build an service for the startup company that contains the data
base of workers, products, clients etc. One of the features of this service is to calculate the
amount of the clients, costumers and of the workers in current season or day or something special 
like holidays. Then we are gonna apply tones of factors, properties, qualities, dependencies and so 
on. Would we put everything of it in the general scope? Of course not.
	In this case we are going to delegate each responsibility to the separate objects with own 
properties and methods. On the way of encapsulating those processes we get rid of complexity, 
unnecessary repeated lines, visibility of privat properties etc...

	Let's take a look at the structure that might be implemented:
For exemple the code should return the total amount of daily salary for current co-worker.

1. Assign the object of particular worker with own parameters(name, position, costumers, sales, hours)
2. Prototype of this object contains the methods allowing us to dynamically store the information and 
execute the calculation of salary amount.
3. Everytime the costumer gets the serving from current worker, we call the method that increase the costumers
value in worker object.
4. Everytime the served costumer buys the product, we call the method that increase the sales value in 
worker object.
5. Also we have to set the Date object to track the worked hours amount. The way to do that is to call the setter
method.
6. Finally, the getSalary method goes through the all of data in object and returns the salary check -
object that contains the name, position of worker and calculated value of daily salary.

	Look, the worker methods and all of processes stays isolated. User is not able to see everything that happens 
inside, its just calls the functions by one simple line.

 
