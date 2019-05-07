# ![LOGO](logo.png) Adyen MarketPay Fund Service MSP Connector

## Description

A generated MSP connector for the Adyen MarketPay Fund Service API (version 3).

Generated from: https://api.apis.guru/v2/specs/adyen.com/FundService/3/openapi.json<br/>
Generated at: 2019-05-07T11:15:12+03:00

## API Description

The MarketPay Funding API provides endpoints for managing the funds in MarketPay accounts. These management operations include actions such as the transfer of funds from one account to another, the payout of funds to an account holder, and the retrieval of balances in an account.

For further information on MarketPay fund management, please visit the [MarketPay documentation](https://docs.adyen.com/developers/marketpay/marketpay-overview).
## Authentication
To connect to the MarketPay API, you must use basic authentication credentials of your web service user. If you don't have one, please contact the [Adyen Support Team](https://support.adyen.com/hc/en-us/requests/new). Then use its credentials to authenticate your request, for example:

```
curl
-U "ws@Company.YourCompany":"YourWsPassword" \
-H "Content-Type: application/json" \
...
```
Note that when going live, you need to generate new web service user credentials to access the [live endpoints](https://docs.adyen.com/developers/api-reference/live-endpoints).

## Versioning
MarketPay API supports versioning of its endpoints through a version suffix in the endpoint URL. This suffix has the following format: "vXX", where XX is the version number.

For example:
```
https://cal-test.adyen.com/cal/services/Fund/v3/accountHolderBalance
```

## Authorization

This API does not require authorization.

## Actions

### Retrieve the balance(s) of an account holder.

> This endpoint is used to retrieve the balance(s) of the accounts of an account holder. An account's balances are on a per-currency basis (i.e., an account may have multiple balances: one per currency).

### Retrieve a list of transactions.

> This endpoint is used to retrieve a list of Transactions for an account holder's accounts. The accounts and Transaction Statuses to be included on the list can be specified. Each call will return a maximum of fifty (50) Transactions per account; in order to retrieve the following set of Transactions another call should be made with the 'page' value incremented. Note that Transactions are ordered with most recent first.

### Disburse a specified amount from an account to the account holder.

> This endpoint is used to pay out a specified amount from an account to the bank account of the account's account holder.

### Refund all transactions of an account since the most recent payout.

> This endpoint is used to refund all the transactions of an account which have taken place since the most recent payout. This request is on a per-account basis (as opposed to a per-payment basis), so only the portion of the payment which was made to the specified account will be refunded. The commission(s), fee(s), and payment(s) to other account(s), will remain in the accounts to which they were sent as designated by the original payment's split details.

### Designate an account to be the beneficiary of a separate account and transfer the benefactor's current balance to the beneficiary.

> This endpoint is used to define a benefactor and a beneficiary relationship between two accounts. At the time of benefactor/beneficiary setup, the funds in the benefactor account are transferred to the beneficiary account, and any further payments to the benefactor account are automatically sent to the beneficiary account. Note that a series of benefactor/beneficiaries may not exceed four (4) beneficiaries and may not have a cycle in it.

### Transfer funds from one marketplace account to another.

> This endpoint is used to transfer funds from one account to another account. Both accounts must be in the same marketplace, but can have different account holders. The transfer must include a transfer code, which should be determined by the marketplace, in compliance with local regulations.

## License

flowground :- Telekom iPaaS / adyen-com-fund-service-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
