Feature: User Login

  Scenario: Login with valid credentials
    Given the user is on the login page
    When they enter a valid email and correct password
    And click the "Login" button
    Then they should be redirected to the homepage
    And they should see their name displayed on the top of the page

  Scenario: Login with invalid credentials
    Given the user is on the login page
    When they enter an incorrect email or password
    And click the "Login" button
    Then they should see an error message "Invalid credentials"

  Scenario: Login with empty fields
    Given the user is on the login page
    When they click the "Login" button without filling in the fields
    Then they should see validation messages indicating required fields