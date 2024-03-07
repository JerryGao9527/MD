# Projects

## 1. LLM 

Working on using fine-tuning an LLM to describe an optimized calendar (like the main takeaways of the optimized calendar)

1. I want an LLM to look at optimized_metrics and optimized_simulated and tell a story based on that
   - For example, Top 3 recommendations in the optimized calendar that affect the profitability of the optimized calendar the most

2. We can also look calendar_compare.csv (not sure we need it) – I am assuming you still remember what these items are

   - We can come up with some test cases of desired stories in certain cases, but I envision a lot of prompt engineering, reinforcement/chatting with LLM is required – you probably can judge better than me

   - I don’t want to compare ref calendar and optimized calendar because ref calendar is most of the time not good quality anyway

   - I just want to display the main takeaways or main recommendations for the optimized calendar for 1 planning account

3. These takeaways would be displayed below or next to the calendar view 

   - Example: few bullet points describing the main drivers for the optimized calendar


   - Example: within each brand, which PPGs are favored in the recommendations – to be promoted a lot


   - Which constraints are limiting these PPGs from even more promotions?


   - Example: within each brand, which PPGs are not favored – not to be promoted as much


   - And maybe why based on the objective, based on profitability, based on constraints, etc.

   - These are just examples; this project is not super clear to me – but I think a pre-trained LLM can reason on the inputs and on the optimized calendar and on the metrics files

## 2. Optimization

Working on the calendar optimization problem by re-engineering how promo offers are fed into the optimizer

1. It requires re-engineering the part of the optimization codebase that enumerates the possible promo offers

   - We have extensive documentation and description for this

   - Promo offer logic itself is simple – enumeration of price points and discount offers

   - But essentially this module is responsible for all the data that is fed into the optimizer – this is about restructuring this entire module


2. We are also looking into moving away from price points to actual promo prices (from .49 to 3.49)

## 3. Outpost

Working on expanding Outpost by introducing a totally new tab for edp optimization (different input files, different LP, different visualizations, etc.)

1. Something users can use independently of TPO (calendar optimization) or in conjunction of TPO

   - Let’s make a distinction: last summer you worked on streamlining, visualizing, improving features for an existing flow or existing capability

   - This project is about building a totally new capability (not features) – its own section on Outpost “Pricing Insights”

     - Takes a small set of inputs from users (1 or 2 tables)

     - Users make click selections on the tab as well

     - A number of recursive optimizations are conducted in the background

     - A plot is displayed (the profitability frontier)

     - Each data point on this frontier curve corresponds to a set of price moves that users can examine by clicking on the specific data point on the plot


     - Essentially, you would be building a data science application from the ground up learning about optimization, input validation, interactive plots and pricing recommendations

   - We have extensive documentation and description for this

2. Pricing insights is a new problem – finding balance between EDLP events (shallow promotions) and GISP (deep promotions)

   - A totally new optimization problem – that requires a new formulation

   - You can use our optimization solvers, but for this, best to use Google OR tools for the linear solver