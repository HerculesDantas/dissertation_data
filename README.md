# Data for the influence
This repository contains the instance data and results for the computational experiments presented in my dissertation. The folders "5.4.1_Computational_Experiments" and "5.4.2_Sensibility_Perishability_Level"  contain the tested instances data and the results for the experiments presented in Sections 5.4.1 and 5.4.2, respectively. 

# Columns dictionary
Both files "results.xlsx" in "5.4.1_Computational_Experiments" and "5.4.2_Sensibility_Perishability_Level" has the same columns structure. Below we present the meaning of each column.

- **Num_Experiment**: Id for experiment. This column was used for the genetic algorithm that need several runs of the same instance for statistical relevance of the results.
- **Char_Optimization_Method**: Solution method
    - Genetic: Genetic algorithm
    - MILP_Callback: Logic-based benders decomposition
    - MILP_Distribution_Only: Model for IPDSP-P that only vehicle routing problem is modeled and the production scheduling follows the same order as the distribution route
    - MILP_No_Callback: Model for IPDSP-P that both production scheduling and vehicle routing problem are modeled
- **Num_Number_Customers**: Number of customers for the instance
- **Num_Time_Limit**: Time limit that model runs
- **Num_Perishability_Level**: Normalized shelf life level
- **Num_Seed**: Seed number that 
- **Num_CPLEX_Status**: CPLEX status. For genetic algorithm uses the default value = 101
- **Num_Run_Time**: Elapsed time to find the optimal solution (when the optimal solution was not proved, Num_Run_Time = Num_Time_Limit)
- **Num_Relative_GAP**: GAP between the best CPLEX solution and the bound. For genetic algorithm uses value 99999
- **Num_Total_Cost**: Objective function value, i.e., total distribution cost
- **Num_Variable_Cost**: Variable cost portion of the objective function
- **Num_Fixed_Cost**: Fixed cost portion of the objective function
- **Num_Number_Vehicles**: Number of vehicles used by the model
- **List_Production_Scheduling**: Python list that contains the production scheduling
- **List_Distribution_Routes**: Python list that contains distribution routes. When the vehicle is not used, the list will appear as [0, n+1], where n is the number of customers for the instance 
