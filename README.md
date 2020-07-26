User stories
Scenario 1: Multi-currency support
Requirments: Aa a customer, I want to be able to pay for products using either British or Euro coins
AC: All British and Euro coins are accepted. 
  
  Given: British currency are added
  When: all the coins are registered
  Then: the customer is allowed to make a purchase from the machine
  
  Given: British currency are added
  When: all the coins are registered
  Then: the customer is allowed to make a purchase from the machine
  
  Given: Non British or Euro currencty has been added
  When: all the coins are registered
  Then: the coins are returned to the user
  
  AC: As coins are entered, the total credit value is uploaded on a display screen.
  
  Given: 50p, 20p, 5p are added to the vending machine
  When: all the coins are registered
  Then: the correct total of 0.75p displayed
  
  Given: 50c, 20c, 10c, 5c are added to the vending machine
  When: all the coins are registered
  Then: the correct total of 0.85c is displayed
  
  Given: invalid currency is added to vending machine
  When: all the coins are registered
  Then: a error message will be displayed
  And: the currency returned
  
  AC: Mixed currency is not accepted; the first coin of the second currency entered does not contribute to the
credit value and is returned to the Customer (with explanation massage on the screen).
  
  Given: British currency is added first followed by Euro currnecy
  When: all the coins are registered
  Then: the error message will be displayed
  And: the Euro currnecy is returned
  
  Given: I have put 50c plus 20p into the vending
  When: all the coins are registered
  Then: the error message will be displayed
  And: the invalid coins returned
  
  Given: British currency plus a invalid currency into the vending machine
  When: all the coins are registered
  Then: the error message will be displayed
  And: the invalid coins are returned
  
  Given: Euro currency plus a invalid currency into the vending machine
  When: all the coins are registered
  Then: the error message will be displayed
  And: the invalid coins returned
  
Questions: 


User stories
Scenario 2: Dispensing change
Requirments: As a coin paying customer, after paying for all my items, I want to be able to receive change.
  AC: After a purchase, the customer’s remaining credit is displayed on the screen. 
  
  Given: X.XX has been put into the vending machine
  When: all items purchased add to less than X.XX
  Then: the correct amount of remaining currency will be displayed
  
  Given: X.XX has been put into the vending machine
  When: all items add to the value £X.XX
  Then: the correct amount of zero remaining currency will be displayed
  
  AC: Change is dispensed at the customer's request.
  
  Given: the correct amount of currency is remaining
  When: the customer requested the remaining credit back
  Then: the correct amount of remaining credit will be returned
  
  Given: there is no due currency remaining
  When: the customer tried to request currency back 
  Then: no currency is returned
 
Questions: 


User stories
Scenario 3: Multiple vends
Requirments: As a coin paying customer, I want to be able to pay for more than one product in a single transaction.
AC: All British and Euro coins are accepted. 
  
  When: I put in british currency
  Then: I am allowed to make a purchase from the machine
  
  When: I put in euro coins
  Then: I am allowed to make a purchase from the machine
  
  When: I put in currency that is not accepted
  Then: the coins are returned to the user
  
Questions: 


User stories
Scenario 4: Contactless payment
Requirments: As a customer, I want to be able to pay for products using contactless debit/credit card or Apple Pay.
AC: The machine will debit the customer’s credit card/bank account with value of selected product.
  
  When: I put in british currency
  Then: I am allowed to make a purchase from the machine
  
  When: I put in euro coins
  Then: I am allowed to make a purchase from the machine
  
  When: I put in currency that is not accepted
  Then: the coins are returned to the user

Questions: 


User stories
Scenario 5: Monitoring & alerting
Requirments: As a Service Operator, I want the machine to notify me of significant/error events
AC: The machine emails designated operative when:
o A product reaches low stock.
o A product goes out of stock.
o The machine temperature goes below or above pre-determined range.
o The machine develops a fault.
  
  When: I put in british currency
  Then: I am allowed to make a purchase from the machine
  
  When: I put in euro coins
  Then: I am allowed to make a purchase from the machine
  
  When: I put in currency that is not accepted
  Then: the coins are returned to the user
  
  
Questions: 
