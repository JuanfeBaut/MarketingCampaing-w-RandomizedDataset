# MarketingCampaing-w-RandomizedDataset
This is a personal project involving data analysis and ML techniques to find client profiles of a fictional sales company named Quantum.

| Column Name | Data Type | Description |
| ----------- | --------- | ----------- |
| CustomerID | Categorical | Unique identifier for each customer |
| Age	| Numerical	| Customer’s age in years |
| AnnualIncome | Numerical | Customer’s annual income (in thousands of USD) |
| SpendingScore	| Numerical | Score from 1 to 100 assigned by the company based on spending behavior |
| WebVisits | Numerical | Total number of visits to the website in the last year |
| DaysSinceLastPurchase | Numerical | Number of days since the customer’s last purchase |
| EmailsOpened | Numerical | Number of marketing emails opened in the last year |
| AdClicks | Numerical | Number of clicks on digital ads in the last year |
| SocialMediaInteractions | Numerical | Number of interactions (likes, comments) on the brand’s social media |
| AvgSessionDuration | Numerical | Average duration of a website session (in minutes) |
| ItemsInCart	Numerical	Average number of items left in the shopping cart |

Due the randomized dataset, the insights I got are only one of the infinite possible outputs

## Code to create and save the dataset

```python
np.random.seed(42)
n_customers = 1000
data = {
'CustomerID': [f'CUST-{i+1:04d}' for i in range(n_customers)],
'Age': np.random.randint(18, 70, size=n_customers),
'AnnualIncome': np.random.randint(20, 150, size=n_customers),
'SpendingScore': np.random.randint(1, 100, size=n_customers),
'WebVisits': np.random.randint(0, 30, size=n_customers),
'DaysSinceLastPurchase': np.random.randint(0, 365, size=n_customers),
'EmailsOpened': np.random.randint(0, 100, size=n_customers),
'AdClicks': np.random.randint(0, 50, size=n_customers),
'SocialMediaInteractions': np.random.randint(0, 200, size=n_customers),
'AvgSessionDuration': np.round(np.random.uniform(1.0, 30.0, size=n_customers), 2),
'ItemsInCart': np.random.randint(0, 15, size=n_customers)
}
df = pd.DataFrame(data)
df.to_csv('quantum_customer_data.csv', index=False)
```

