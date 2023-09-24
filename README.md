# Titanic MOGP 

## VIP Bootcamp

Working with Titanic dataset and multi objective GP. 🚢

## Constraints

1. We can:
   - Use strongly typed GP to predict boolean answers.
   - Use strongly typed GP to predict float answers, then convert the floats to booleans in your evaluation function (e.g., >0 or <0 for 0 and 1).
   - Work with loosely typed GP and manage the results in your evaluation function.
   
2. **Don't** use methods from [here](https://deap.readthedocs.io/en/master/api/algo.html).

   |     method name   |   Usage/Returns   |
   | ------------- | ------------- |
   | deap.algorithms.eaSimple(population, toolbox, cxpb, mutpb, ngen[, stats, halloffame, verbose])| A class:~deap.tools.Logbook with the statistics of the evolution  |
   |deap.algorithms.eaMuPlusLambda(population, toolbox, mu, lambda_, cxpb, mutpb, ngen[, stats, halloffame, verbose])| ^^ |
   |deap.algorithms.eaMuCommaLambda(population, toolbox, mu, lambda_, cxpb, mutpb, ngen[, stats, halloffame, verbose])| ^^|
   |deap.algorithms.eaGenerateUpdate(toolbox, ngen[, stats, halloffame, verbose])| ^^|
   |deap.algorithms.varAnd(population, toolbox, cxpb, mutpb)|A list of varied individuals that are independent of their parents.|
   |deap.algorithms.varOr(population, toolbox, lambda_, cxpb, mutpb)| The final population.|
   |class deap.cma.Strategy(centroid, sigma[, **kargs])[source]| |
   |class deap.cma.StrategyOnePlusLambda(parent, sigma[, **kargs])| |
   |class deap.cma.StrategyMultiObjective(population, sigma[, **kargs])| |
   
   
   

4. Upload a single CSV file with predictions on `test.csv` for each Pareto optimal individual you unearth from the `train.csv` in separate columns. Reuse the preprocessed and folded data from the Titanic ML assignment.
5. On DEAP when we look at the fitness of our MOGA, we use `individual.fitness.values` to see how fit our individuals are. We must assign it in the eval function/main loop. By taking in the individual itself, we modify/return the mutant. We must build the truth data so that we can pass features through/get predictions.

## 📢 Presentation Details

- **Data Processing**: EDA and our preprocessing from last assignment
- **ML Algorithms**: On how we got the final Pareto-optimal set.
- **Evolutionary Algorithm Design**: evolutionary algorithm's architecture. Describe algorithm design iterations, AAD focus
- **Comparison Time**: BOBB on DEAP, we benchmark against our own models from last week, (random forest, xgboost, log regression, etc.)
