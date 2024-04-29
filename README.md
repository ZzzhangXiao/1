## American Express Innovation Labs AI Hackathon (Singapore) 2024 
### Background:
- American Express has a Merchant Recommender to help connect an Amex Credit Card Customer with an Amex Merchant (Shop that accepts Amex cards)
- This capability recommends (show on a marketing channel) personalizedmerchants to Customers, to help Customers discover merchants near to them to shop & increase spend on merchants. These recommended merchants are decided by an algorithm.
- A Customer transacting on a recommended merchant within 30 days of recommendation date is tagged as a successful activation.
- However, a Customer could have transacted with merchants even though it was not recommended by Amex (oragnic activation). Think about all the shops you visit without these shops being marketed to you

## Problem Statemene:
The goal is to find merchants for each customer that have maximum 'incremental activations' (and hence minimum organic activations). Incremental Activations means activations on merchants that the Customer would not have discovered otherwise, unless recommended.

## Evaluation Criteria:
- Some Merchants are randomly Recommended & Not-Recommended at the Customer level.
- The goal is to maximize Incremental Activation on Top 10 merchants by prediction for each Customer (collated at a dataset level)
- Incremental Activation rate = Recommended Activation Rate minus Not-Recommended Activation Rate.
- Activation rate = No. of Activations/No. of Recommendations, at Customer x Merchant level.

  ## Expected outcome:
  For each Customer x Merchant combination in Round 1 submission data, calculate a score such that Incremental Activation Rate on Top 10 merchants by prediction for each Customer (collated at a dataset level) is maximized. The final output file to be uploaded should have 3 columns - Customer, Merchant & predicted_score
  

- Participants will train their model using labeled Training Data
- Participants are free to split the training data into Train & Out-of-sample/In-time data into whatever ratio they deem fit. They are also free to use any sampling technique on Train data*
- An evaluation custom code (in Python) to calculate the " Incremental Activation Rate (at dataset level) on Top 10 merchants (by prediction) for each Customer" would be provided to participants to run on their training/out-of-sample data scores to mimic the exact evaluation process that will run on their submitted Round 1 data.
- Directions to run the code have been mentioned at the beginning of the code. This code cannot be used on scored Round 1 submission data as it doesn't have the 'activation' column.
- Once participants have the best model according to them, they can score the Round 1 submission data and upload it.
- Scored Round 1 submission data should be a CSV & delimited by ",". The first row should be the header with column names: customer, merchant & predicted_score. None of these 3 columns can be missing/null/ na etc.
- Scored Round 1 submission data should have only 3 columns and the unique Customer x Merchant count should be 12,604,600.
- The top 15 Teams with the Highest " Incremental Activation Rate on Top 10 merchants by a prediction for each Customer (Leaderboard + Closed evaluation datasets)" will be shortlisted for Round 2.
- Train data has already been sampled once before sharing, hence will contain < 100 merchants per Customer
