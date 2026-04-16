Feature: Free Shipping

  Scenario: Apply free shipping for orders above €50
    Given the user has added products to the cart totaling €60
    When they view the cart
    Then the shipping cost should be displayed as "Free"

  Scenario: Do not apply free shipping for orders below €50
    Given the user has added products to the cart totaling €30
    When they view the cart
    Then the shipping cost should be displayed with the standard rate

  Scenario: Apply free shipping exactly at the minimum threshold
    Given the user has added products to the cart totaling €50
    When they view the cart
    Then the shipping cost should be displayed as "Free"