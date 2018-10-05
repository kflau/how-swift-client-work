# how-swift-client-work

This is a 5-minute tutorial showing how to bootstrap a SWIFT Java client.

## Getting Started

Add [prowide-core] in build.gradle.

## SWIFT Explained

Most international transfers are executed through SWIFT, a co-operative society, founded in 1974 by seven international banks, which operate a global network to facilitate the transfer of financial messages. Using these messages, banks can exchange data for funds transfer between financial institutions. See SWIFT.

```
+-------------------------------------------------------------------------+
|             MT103                                                       |
|    +------------------> BIC                                             |
|    |                     +               BIC                            |
|    +                     |                                              |
|   BIC                    |                                   BIC        |
|                          |                                              |
|       BIC                +----------------------> BIC                   |
|                                                    +                    |
|                                                    |                    |
|                                                    |                    |
|                                     BIC            |              BIC   |
|       BIC                                          |                    |
|                         BIC                        v                    |
|                                                    BIC                  |
+-------------------------------------------------------------------------+
```

Each financial institution is provided an ISO 9362 code, also called a Bank Identifier Code (BIC) or SWIFT Code. These codes generally are eight characters long. For example: Deutsche Bank is an international bank, with its head office in Frankfurt, Germany, the SWIFT Code for which is DEUTDEFF:

DEUT identifies Deutsche Bank.

DE is the country code for Germany.

FF is the code for Frankfurt.

Using an extended code of 11 digits (if the receiving bank has assigned extended codes to branches or to processing areas) allows the payment to be directed to a specific office. For example: DEUTDEFF500 would direct the payment to an office of Deutsche Bank in Bad Homburg.

European banks making transfers within the European Union also use the International Bank Account Number, or IBAN.

Different message types are supported

| Category      | Description                              | Model classes  |
| ------------- |:----------------------------------------:| --------------:|
| 0             | System Messages                          |    MT0nn       |
| 1             | Customer Payments                        |    MT1nn       |
| 2             | Financial Institution Transfers          |    MT2nn       |
| 3             | MT3nn - FX, Money Market & Derivatives   |    MT3nn       |
| 4             | Collections and cash letters             |    MT4nn       |
| 5             | Securities Markets                       |    MT5nn       |
| 6             | Precious Metals & Syndications           |    MT6nn       |
| 7             | Documentary Credits & Guarantees         |    MT7nn       |
| 8             | Travellers Cheques                       |    MT8nn       |
| 9             | Cash Management & Customer Status        |    MT9nn       |

[prowide-core]: https://github.com/prowide/prowide-core
