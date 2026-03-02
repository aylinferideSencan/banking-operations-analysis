import pandas as pd

# Sample banking transaction data
data = {
    "Transaction_ID": [1, 2, 3, 4, 5, 6],
    "Channel": ["Mobile", "ATM", "Web", "Mobile", "Web", "ATM"],
    "Transaction_Type": ["Transfer", "Withdrawal", "Payment", "Transfer", "Payment", "Withdrawal"],
    "Status": ["Success", "Failed", "Success", "Success", "Failed", "Success"]
}

df = pd.DataFrame(data)

# Basic analysis
total_transactions = len(df)
successful_transactions = df[df["Status"] == "Success"].shape[0]
failed_transactions = df[df["Status"] == "Failed"].shape[0]

channel_summary = df.groupby("Channel").size()

print("Total Transactions:", total_transactions)
print("Successful Transactions:", successful_transactions)
print("Failed Transactions:", failed_transactions)
print("\nTransactions by Channel:")
print(channel_summary)



# Banking Operations Analysis

This project demonstrates a simple analysis of banking transaction data.

## Purpose
To monitor basic operational metrics such as:
- Total transactions
- Success and failure rates
- Transaction distribution by channel

## Tools
- Python
- Pandas

## Outcome
This analysis helps understand transaction performance and identify operational issues in digital banking channels.

“Basit bir işlem verisiyle
başarılı–hatalı işlem sayılarını çıkardım
ve hangi kanalda sorun yoğun onu görmek istedim.”
