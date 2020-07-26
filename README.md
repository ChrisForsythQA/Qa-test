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
  
  Given: Non British or Euro currency has been added
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
  
AC: Mixed currency is not accepted; the first coin of the second currency entered does not contribute to the credit value and is returned to the Customer (with explanation message on the screen).
  
  Given: British currency is added first followed by Euro currnecy
  When: all the coins are registered
  Then: the error message will be displayed
  And: the Euro currnecy is returned
  
  Given: I have put 50c plus 20p into the vending
  When: all the coins are registered
  Then: the error message will be displayed
  And: the invalid coins returned
  
  Given: British currency plus a invalid currency added to the vending machine
  When: all the coins are registered
  Then: the error message will be displayed
  And: the invalid coins are returned
  
  Given: Euro currency plus a invalid currency added to the vending machine
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
  
  When: all items add to the value £X.XX
  Then: the correct amount of zero remaining currency will be displayed
  
AC: Change is dispensed at the customer's request.
  
  Given: the correct amount of currency is remaining
  When: the customer requests the remaining credit back
  Then: the correct amount of remaining credit will be returned
  
  Given: there is no due currency remaining
  When: the customer tries to request currency back 
  Then: no currency is returned
  
AC: Change is returned in the smallest number of coins.

  Given: there is 0.25 currency remaining
  When: the customer requests remaining currency back 
  Then: 0.20
  And: 0.05 currency will be returned (2 coins)
  
  Given: there is 1.65 currency remaining
  When: the customer requests remaining currency back 
  Then: 1.00, 0.50, 0.10
  And: 0.05 currency coins will be returned (4 coins)
  
AC: The customer is notified about how much change has been dispensed on the display screen.

  Given: there is X credit remaining
  When: the credit is returned to the customer
  Then: the returning credit will be displayed correctly
  
AC: If the machine is unable to offer change, the customer must be notified of this via the display screen prior to
making a purchase. 

  Given: there is insufficient change in the vending machine
  Then: a message will be displayed to the customer
  
  Given: the customer purchases a item/s
  And: there is remaining credit
  When: the customer tries to returned the credit
  Then: a message will be displayed of insufficient change to return
 
Questions: Will enough change be returned to customer as possible?


User stories
Scenario 3: Multiple vends
Requirments: As a coin paying customer, I want to be able to pay for more than one product in a single transaction.
AC: To enable multi-product purchase, change is not dispensed immediately after the customer pays for the first product 
  
  Given: there is sufficient amount of credit
  When: the customer purchases 1 item
  Then: the item will be dispatched
  And: any remaining credit will not be returned
  
  Given: there is sufficient credit remaining
  When: the customer purchases another item
  Then: the item will be dispatched
  And: any remaining credit will not be returned
  
  Given: there is insufficient amount of currency remaining
  When: the customer tries to purchase
  Then: no purchase can be made
  And: remaining currency returned at request
  
AC: Credit must be displayed on the display screen.

  Given: there is X amount of currency added
  When: all coins have been registered
  Then: the correct amount of credit will be displayed
  
  Given: there is X amount of currency
  When: the customer purchases 1 item
  Then: the correct amount of credit will be displayed
  
  Given: there is sufficient remaining credit
  When: the customer purchases another item
  Then: the correct amount of credit will be displayed
  
  Given: there is insufficient remaining credit
  When: the customer tries to purchase another item
  Then: a message of insufficient funds will be displayed
  And: remaining credit dispalyed
  
Questions: Will enough change be returned to customer as possible?


User stories
Scenario 4: Contactless payment
Requirments: As a customer, I want to be able to pay for products using contactless debit/credit card or Apple Pay.
AC: The machine will debit the customer’s credit card/bank account with value of selected product.
  
  Given: a valid contactless payment has been scanned
  When: the customer selects an item
  Then: the item will be dispatched to the customer
  
  Given: a valid contactless payment has been scanned
  When: the customer selects an item
  And: there is insufficient funds
  Then: a error message will be displayed

Questions: Can customer add multiple items before purchase or have to purchase individually? Does the card/apple pay need to be scanned before or after selecting item/s? Will there be a message for insufficient funds?


User stories
Scenario 5: Monitoring & alerting
Requirments: As a Service Operator, I want the machine to notify me of significant/error events
AC: The machine emails designated operative when:
o A product reaches low stock.

  Given: product stock is set a X amount
  When: the stock hits X
  Then: a low stock notification will be sent
  
o A product goes out of stock.

  Given: product stock is set a X amount
  When: the stock hits 0
  Then: a out of stock notification will be sent
  
o The machine temperature goes below or above pre-determined range.

  Given: the vending machine is set a X tempature
  When: the temperture goes below X
  Then: a warniing notification will be sent

o The machine develops a fault.
  
  When: I put in british currency
  Then: I am allowed to make a purchase from the machine
  
  When: I put in euro coins
  Then: I am allowed to make a purchase from the machine
  
  When: I put in currency that is not accepted
  Then: the coins are returned to the user
  
  
Questions: 
