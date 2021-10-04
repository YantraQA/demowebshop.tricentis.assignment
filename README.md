# demowebshop.tricentis.assignment
Automation Assignment

### URL: http://demowebshop.tricentis.com/

#### Scenario to Automate
* Note: Write more smaller test cases for validations like Search, add/remove products from cart etc

```gherkin
    Scenario: End to End User journey for buying a product
      Given I have on the landing page of the application
        * I register as a new user
        * I search for a product
        * I add the product to the basket with quantity as 2
        * I navigate to the cart
        * I checkout the cart
        * I add billing address as below and proceed next
          |FirstName| Shahrukh|
          |SecondName| Khan   |
          |Country   | India  |
          |City      |Mumbai  |
          |Address   | Manant |
          | zipCode  | 32244  |
          |phone     |34335   |
        * I select shipping address same as Billing address and proceed next
        * I select Shipping Method as "Next Day Air" and proceed next
        * I select payment method as "Purchase Order" and proceed next
        * I enter Payment Number as "12345" and process next
      When I enter confirm order
      Then Order is successfully placed and Thank you message is displayed
      And Order number is displayed
```

#### Rules:
* Java Maven project
* Use Page object model, different java page object classes for each of pages
* Use Log4j2 for logging
* Use Extent Report for HTML report
* Use Lombok library to eleminate any boiler plate code
* Create Multiple Step Definition files
* Use pico container for dependency Injection

#### Hints:
  * Start Simple
  * Create a simple java maven project and add depdencies in pom.xml
  * Create a feature file and add above sceanrio
  * Generate a step def file
  * Keep only one step def file in the begininig
  * Do not use page object model in the begininnig if you find it confusing
  * First just do everything in a same step def file and use driver.findelement to perform operation
  * Once all the steps are done then start implementing page object files for each pages and moving ur locators in the page object model file.
  * Once this is also done then Create Test Context class and start implementing multiple Step defs, move step def methods in the correct step def class files and bind them with DI pico container FW.

