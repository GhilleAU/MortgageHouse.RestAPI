# MortgageHouse.RestAPI

Minimal .NET Core Web API that exposes a GET endpoint to retrieve mock loan rate data based on loan type and term.

## Features

- Single endpoint: `GET /api/rates`
- Query parameters:
  - `loanType` (string): e.g., `owner-occupied`
  - `term` (int): e.g., `15`, `30`

- Returns mock JSON loan rate data

## Prerequisites

- [.NET SDK 6.0+](https://dotnet.microsoft.com/en-us/download)

## Example

- **Query Url** 
  - `/api/rates?loanType=owner-occupied&term=30`
- **Query Response**
```json
[
    {
        "loanType": "owner-occupied",
        "term": 30,
        "interestRate": 6.25,
        "comparisonRate": 6.3,
        "lender": "Mortgage House",
        "monthlyRepayment": 2150.75
    },
    {
        "loanType": "owner-occupied",
        "term": 30,
        "interestRate": 6.1,
        "comparisonRate": 6.15,
        "lender": "Mortgage House",
        "monthlyRepayment": 2100.5
    }
]
```
