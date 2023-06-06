<p align="center"><a href="https://pluton.ltd/" target="_blank"><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAE0AAABGCAYAAACJzhlzAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAARMSURBVHgB7Zz9WRpBEMZf8uT/2EE2HUgH0IFUIFQQrUCsAK0ArEA7gFSgHdylAu1gMuPuKpLA7d7t1wV/zzPAg/f5MrM7uzsnUAhENGJbslX0zqP5TuGTd0QQtjU1c4VP3gSryJ0ljh1PwSwLHCt88xfUHoVjpKWXWW5wbPBNn1I3KmTkC/Kg0A2FjOQS7QQ9JpdoT+jGCzKSS7Qa3W78F1pg2tL+ejlf/IracwZPjGDPpHtthT5CejTwTP48whPe53znXJWIiD5C/glu5eslvP3PPccSEc+REj7hGelZCIUOeAhXtRDsyuG4aSYC/vHrdTox6VBdHfCIOXk24I6CpRGOT7DYc+KKunvdCel5tamxVu3OgWs8xD2F7lnNDa0dTr6gTN26ucYltaeiUD0r+c97ybYjJMQI9kjdqToLRzq/qagdSbyO9I8aQjCLtKPeuaC9mHNql0ttU7FNEQnyjwIf/DoI8ut9XFhS4Eyc4gpmcROO2vU+LlQUyOvofViUgv09K7n3kF1ZUgevI52WpBLMUv11zZTG1XcvYgpPSLezuajIehyldfVdluTodRS+nW3Dae5fzlJRg9dRGYIJ32UScoX81If+SLoHm6MQviIvG7brwWCw2bcB6VX1KQoih2gyzf3AdtcgljS492wjFEZK0USsW7YbFuvg+oARbM1W5OxqCtFqtjs4iCWQ7klFMIVCGUh3gDhs0NBe7dILwZgYS3gbtjEfe+wpmIRi0YJZQoenl1CWLcF6sSYZ2tPuyXOKmvSKUG8EE2K1aVP2uLumjUwvKeuYCj0hVpsmrMhhHsr0pmM0jAhKI2Ytx9xRuJrtB3+8Rvm8pkyxC2BEOKcaWRZuzm8TlO11SUQTZAV9TQ4LLCycDK8kXDcomFSlViM2pxIGE64iXLHhmrI+TbGtyXHC0YSrtHU1CiN1UZ+Cn3A1dLg2pi8pyVEJqaBDdeSysQnXKX+8ROayUUvOQmXxuAvXHVg4eXZgiLzhWstLLtEsC/JYxd7K6W6RkdyiCXPyXP5n4cRDZ8jkdSWIJjgnwRYWboVMQ7BSRBOck2BLriFYSaIJIzgmwduYnC6Z15UmmqDgkctZzOSnCPeAyJQomqCghfOa0DThKoP+WOFay0upogkvaJnMxh6ClSqa5GFjM4xqhdlXkuHgQ7DSRHudyZU8zGWNtAk5RowhWEmibdiGbVazmjBDsAkCUYpol2adtEY8gj0HlbtqqGabsFhPiAjp2rcpuvNbXnJ6mjT2wwSCKX4L+uxTrlKrSzN2TIEIphCQ1KKJV00it11vBAzLD6QMz1sWa5hQMIXAYWlJVZ82i5FKNBA8LC2xRdtAh2PSuf1YYYnIi8W2sR9nEEwhUljCiBbD02okyL0OEC0sLaE9LUnutQ/Sz2hOEZlQniZuOzO1GFkw0+RJ/iHdVylSw3+AtJ0s3Gzna7X1+QQfqy3l87c92x7c9w9HwlVSSMWPEwAAAABJRU5ErkJggg==" width="400"></a></p>

## Aspire Challenge

### Setup procedure
1. Fork the repository in your personal github account
2. Checkout a new feature branch from `main`
3. Complete the test in 2h and 30min
4. Push the code and prepare the Pull Request from feature branch to main branch

### Test #01
#### Objective
Create feature *DebitCard* and *DebitCardTransaction* endpoints and relatives policies, validations and resources.

#### Business Logic
Each customer can have multiple *Debit Cards* and each debit card can have many *Debit Card Transactions*.

- The customer should be able to create, update, read and delete his debit cards. 
- For each debit card the customer should be able to read and create debit card transactions.

##### Debit cards endpoints:
- **get** `/debit-cards`
- **post** `/debit-cards`
- **get** `/debit-cards/{debitCard}`
- **put** `/debit-cards/{debitCard}`
- **delete** `/debit-cards/{debitCard}`

##### Debit card transactions endpoints *(optional/bonus point)*:
- **get** `/debit-card-transactions`
- **post** `/debit-card-transactions`
- **get** `/debit-card-transactions/{debitCardTransaction}`

#### Challenge
Create the *DebitCard* and *DebitCardTransaction* routes, controllers, requests, resources and policies. 
Create your own logic.

Tips:
- customer can handle only his own debit cards


---

### Test #02

#### Objective
Create a Loan service to handle repayments based.

#### Business Logic
Each customer can have a credit *loan* (due in 3 or 6 months). So a Loan has 3 or 6 *scheduled repayments* (once each month),
and it can be repaid with *received repayments*.
Example:

Loan of 3 months, amount 3000$, created on 2021-01-01
- Scheduled Repayment of 1000$ due to 2021-02-01
- Scheduled Repayment of 1000$ due to 2021-03-01
- Scheduled Repayment of 1000$ due to 2021-04-01

A customer can repay the full amount of each single scheduled repayment, but also he can repay partially or in full

#### Challenge
Read through the tests of LoanService to understand what is the logic to be implemented. All classes and files are already created, you just need to complete them.
In order to make the unit tests passed, you need to fulfil:
- the migrations/factories for scheduled_repayments and received_repayment tables (migration for loans table already done);
