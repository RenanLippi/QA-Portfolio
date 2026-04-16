Feature: Shopping Cart

  Scenario: Add product to cart
    Given the user is on a product page
    When they click the "Add to cart" button
    Then the product should be added to the cart
    And the cart counter should be updated

  Scenario: Remove product from cart
    Given the user has a product in the cart
    When they click the "Remove" button
    Then the product should be removed from the cart
    And the cart should reflect that it is empty