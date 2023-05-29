# -WhiskasModel
Mini case/Team 3
What are the two parameters that the LpProblem function implements?
The LpProblem function takes two parameters. The initial parameter is the name of the problem, referred to as "The Whiskas Problem," which is a string data type commonly used in programming to represent text. The second parameter can be either LpMinimize or LpMaximize, depending on the type of Lp problem we aim to solve. In this particular case, we are using LpMinimize. Therefore, the parameters would be defined as follows:
prob = LpProblem
Is it mandatory to name the prob variable as prob?
No, it is not mandatory to name the problem variable as "prob" in programming. The choice of variable names is typically up to the programmer and can be chosen based on readability and clarity. However it is the most commonly used.
What are LpContinous and LpInteger used for? (paulina)
The variable LpContinuous is used to represent the amount of beef in the cat food. It can take any value in a specific range, such as 0%, 25%, 50%, or even 100%. Since it is a continuous variable, it can be any real number between 0 and 100. This means that you could choose, for example, to use 37.5% beef in the cat food.
On the other hand, the variable LpInteger is used to represent the amount of chicken in the cat food. Unlike the previous variable, this variable can only take integer values, that is, numbers without decimals. This means that you can only choose amounts such as 0%, 10%, 30% or 100% chicken. You cannot use a value like 27.5%, since it is not an integer.
Using these two types of variables, you can more accurately model the amount of chicken and beef in the cat food. 


Explain and copy the section of code that defines the objective function. 
Information is being added to the variable "prob" using the "+=" operator. The variable "prob" is likely associated with an optimization problem or mathematical modeling.
The expression "0.013 * x + 0.008 * x2" represents the objective function itself. This objective function is a linear combination of two variables, "x" and "x2". Each variable is multiplied by a respective coefficient (0.013 and 0.008) that determines the relative importance of each variable in the objective function.
After the objective function, there is a string of text, "Total Cost of Ingredients per can", which provides a brief description of what the objective function represents. This description can be helpful for understanding the context of the problem or providing additional information about the objective function.
	The objective function becomes:
				min 0.013X1 + 0.008X2
Code:
The variable “prob” begins collecting problem data with the “+=” operator. The objective function is logically entered first, with an important comma”,” at the end of the statement and short string explaining what this objective function is:
prob  += 0.013 * x + 0.008 * x2, “ Total Cost of Ingredients per can”
Explain and copy the section of code that defines the constraints. 
The constraints are the limitations or restrictions on the decision variables. They limit the value of the decision variables, also they must sum 100 and that the nutritional requirements are met. 
The constraints are the following: 
1.000x1+1.000x2 =100.0
0.100x1+0.200x2 ≥8.0
0.080x1+0.100x2 ≥6.0
0.001x1+0.005x2 ≤2.0
0.002x1+0.005x2 ≤0.4


Is this a minimization or maximization problem? 
IIt's a minimization problem, because the goal is to reduce the cost of the ingredients for the can of cat food, that minimize cost while satisfying the given constraints.
Run the WhiskasModel1.py code. (no need to make changes, just run it as is) What is the value of the following variables. Status: BeefPercent = ChickenPercent = Total Cost of Ingredients per can =
Beef Percent= 66
Chicken Percent= 34
Total Cost of Ingredients per can= .97
