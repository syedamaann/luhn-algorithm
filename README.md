# Luhn Algorithm Implementation

This Python script implements the Luhn algorithm, a checksum formula used to validate identification numbers like credit card numbers.

## How it Works

The Luhn algorithm detects common errors in identification numbers by doubling every second digit, adjusting numbers greater than 9, and checking if the total sum is divisible by 10.

### Credit Card Number Structure

The structure of credit card numbers adheres to industry standards (ISO/IEC 7812) with variations among issuers (e.g., Visa, Mastercard). Here's a simplified breakdown:

- **Issuer Identification Number (IIN) or Bank Identification Number (BIN):**
  - The first few digits (typically 6) identify the card issuer or issuing bank.

- **Account Number:**
  - The subsequent digits (excluding the last one) uniquely identify the account.

- **Checksum Digit:**
  - The last digit is calculated using the Luhn algorithm to ensure the number's integrity.

### Luhn Algorithm Steps

1. **Doubling and Adjusting Digits:**
    - Starting from the right (excluding the checksum digit), double every second digit.
    - If doubling results in a number greater than 9, subtract 9.

2. **Summation:**
    - Sum all digits, including the unchanged odd digits and the modified even digits.

3. **Checksum Verification:**
    - Check if the total sum is divisible by 10.

### Usage

1. **Setup**
    - Ensure Python is installed on your system.

2. **Running the Script**
    - Open `luhn_algorithm.py` in a Python environment or text editor.

3. **Validating a Credit Card Number**
    - Modify `credit_card_number` with the number you want to validate.
    - Run the script.
    - If the credit card number is valid, it prints "Valid credit card number."
    - If invalid, it prints "Invalid credit card number."

## Example

```python
credit_card_number = '4111-1111-4555-1142'
translated_card_number = credit_card_number.replace('-', '').replace(' ', '')

if is_valid_credit_card_number(translated_card_number):
    print("Valid credit card number.")
else:
    print("Invalid credit card number.")
```

Output:
```
Valid credit card number.
```
